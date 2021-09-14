---
title: Cómo crear un cuadro de lista simple
description: En este tema se muestra cómo inicializar y recuperar elementos de un cuadro de lista simple.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062228"
---
# <a name="how-to-create-a-simple-list-box"></a>Cómo crear un cuadro de lista simple

En este tema se muestra cómo inicializar y recuperar elementos de un cuadro de lista simple.

El ejemplo de código de C++ de este tema incluye un procedimiento de cuadro de diálogo que rellena un cuadro de lista con información sobre los jugadores de un equipo deportivo. Cuando el usuario selecciona el nombre de un jugador de la lista, se muestra información sobre el reproductor en el cuadro de diálogo. El estilo de ventana del cuadro de lista incluye [**LBS \_ SORT**](list-box-styles.md), lo que da como resultado una lista ordenada de elementos. En la siguiente captura de pantalla se muestra el cuadro de diálogo.

![captura de pantalla de un cuadro de diálogo que contiene un cuadro de lista etiquetado, texto sobre el elemento de cuadro de lista seleccionado y un botón Aceptar](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


La aplicación debe realizar las siguientes tareas relacionadas con el cuadro de lista:

-   Inicialización del cuadro de lista
-   Recuperación de la selección del usuario desde el cuadro de lista

En el siguiente ejemplo de código de C++, la información sobre los reproductores se almacena en una matriz de estructuras. Durante la inicialización, el procedimiento del cuadro de diálogo usa el mensaje [**\_ ADDSTRING**](lb-addstring.md) de LB para agregar los nombres de los miembros del equipo al cuadro de lista (EJEMPLO **DE \_ LISTBOX \_ de IDC)** de uno en uno. También usa el mensaje [**\_ LB SETITEMDATA para**](lb-setitemdata.md) agregar el índice de matriz del reproductor al cuadro de lista como datos de elemento. Más adelante, cuando el usuario selecciona un reproductor del cuadro de lista, el procedimiento del cuadro de diálogo usa el mensaje [**\_ GETITEMDATA de LB**](lb-getitemdata.md) para recuperar el índice de matriz correspondiente. A continuación, usa el índice de la matriz para recuperar información del reproductor de la matriz.



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

[Referencia del control List Box](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Acerca de los cuadros de lista](about-list-boxes.md)
</dt> <dt>

[Usar cuadros de lista](using-list-boxes.md)
</dt> </dl>

 

 




