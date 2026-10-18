# B2B Lead-to-Order Business Process Flow

## Overview
This flowchart defines the standard B2B lifecycle from multi-channel lead ingestion, qualification, deduplication, opportunity management, through to ERP invoice and order creation.

## Process Flowchart
```mermaid
flowchart TD
    A([ליד חדש נכנס: טופס אתר / קמפיין]) --> B{ולידציה: פרטים מלאים ותקינים?}
    B -- לא --> C[סטטוס: פסול / חסר פרטים]
    B -- כן --> D{בדיקת כפילויות מול מאגר קיים}
    
    D -- קיים במערכת --> E[מיזוג רשומות ושיוך לאיש המכירות המטפל]
    D -- לקוח חדש --> F[יצירת רשומת Lead חדשה והקצאה לפי אזור/תחום]
    
    F --> G[שיחת בירור צרכים והסמכה - Qualification]
    G --> H{האם יש תקציב וצורך מיידי?}
    H -- לא --> I[סטטוס: מעקב עתידי / Nurturing]
    H -- כן --> J[המרת ליד: יצירת Account + Contact + Opportunity]
    
    J --> K[אפיון צרכים והפקת הצעת מחיר במערכת]
    K --> L{האם הלקוח אישר את ההצעה?}
    L -- נדחה / לא נסגר --> M[סטטוס: Closed Lost - תיעוד סיבת הפסד]
    L -- אושר --> N[סטטוס: Closed Won - מעבר ל-ERP]
    
    N --> O[פתיחת כרטיס לקוח ב-ERP, הפקת הזמנת עבודה וחשבונית]
```
