---
title: Cómo crear un cuadro de lista simple
description: En este tema se muestra cómo inicializar y recuperar elementos de un cuadro de lista simple.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078613"
---
# <a name="how-to-create-a-simple-list-box"></a>Cómo crear un cuadro de lista simple

En este tema se muestra cómo inicializar y recuperar elementos de un cuadro de lista simple.

El ejemplo de código de C++ de este tema incluye un procedimiento de cuadro de diálogo que rellena un cuadro de lista con información sobre jugadores en un equipo deportivo. Cuando el usuario selecciona el nombre de un reproductor de la lista, se muestra información sobre el reproductor en el cuadro de diálogo. El estilo de ventana del cuadro de lista incluye la [**\_ ordenación lbs**](list-box-styles.md), lo que da como resultado una lista ordenada de elementos. En la captura de pantalla siguiente se muestra el cuadro de diálogo.

![captura de pantalla de un cuadro de diálogo que contiene un cuadro de lista con etiqueta, texto sobre el elemento de cuadro de lista seleccionado y un botón Aceptar](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


La aplicación debe realizar las siguientes tareas relacionadas con el cuadro de lista:

-   Inicializar el cuadro de lista
-   Recuperar la selección del usuario del cuadro de lista

En el siguiente ejemplo de código de C++, la información acerca de los reproductores se almacena en una matriz de estructuras. Durante la inicialización, el procedimiento de cuadro de diálogo utiliza el mensaje de [**lb en lb \_**](lb-addstring.md) para agregar a la vez los nombres de los miembros del equipo al cuadro de lista (ejemplo de un **\_ control \_ IDC**). También usa el mensaje [**lb \_ SETITEMDATA**](lb-setitemdata.md) para agregar el índice de la matriz del reproductor al cuadro de lista como datos de elemento. Más adelante, cuando el usuario selecciona un reproductor en el cuadro de lista, el procedimiento de cuadro de diálogo utiliza el mensaje [**lb \_ GETITEMDATA**](lb-getitemdata.md) para recuperar el índice de la matriz correspondiente. A continuación, usa el índice de la matriz para recuperar la información del reproductor de la matriz.



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de cuadro de lista](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Acerca de los cuadros de lista](about-list-boxes.md)
</dt> <dt>

[Usar cuadros de lista](using-list-boxes.md)
</dt> </dl>

 

 




