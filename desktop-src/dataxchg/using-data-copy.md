---
title: Uso de la copia de datos
description: En este tema se proporciona un ejemplo que muestra cómo enviar información entre dos aplicaciones.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Interfaz de usuario de Windows, copia de datos
- copia de datos, ejemplos
- copia de datos, mensaje de WM_COPYDATA
- Mensaje WM_COPYDATA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e44c4abb9aba68d4db1544f5c7d52220cdc681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704971"
---
# <a name="using-data-copy"></a><span data-ttu-id="b3117-107">Uso de la copia de datos</span><span class="sxs-lookup"><span data-stu-id="b3117-107">Using Data Copy</span></span>

<span data-ttu-id="b3117-108">En el ejemplo siguiente se muestra cómo enviar información entre dos aplicaciones mediante el mensaje de [**\_ COPYDATA de WM**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="b3117-108">The following example demonstrates how to send information between two applications using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span>

<span data-ttu-id="b3117-109">La aplicación de envío muestra al usuario un cuadro de diálogo que solicita cierta información.</span><span class="sxs-lookup"><span data-stu-id="b3117-109">The sending application displays a dialog box to the user which requests certain information.</span></span> <span data-ttu-id="b3117-110">La aplicación empaqueta la información en una estructura de datos privada, incluye un puntero a la estructura en la estructura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) y envía la información a la aplicación receptora mediante el mensaje [**\_ COPYDATA de WM**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="b3117-110">The application packages the information into a private data structure, includes a pointer to the structure in the [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure, and sends the information to the receiving application using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span> <span data-ttu-id="b3117-111">La aplicación receptora tiene una ventana oculta con el nombre de clase Disp32Class.</span><span class="sxs-lookup"><span data-stu-id="b3117-111">The receiving application has a hidden window with the class name Disp32Class.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



<span data-ttu-id="b3117-112">La aplicación receptora tiene una ventana oculta que recibe la información de [**WM \_ COPYDATA**](wm-copydata.md) y la muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="b3117-112">The receiving application has a hidden window which receives the information from [**WM\_COPYDATA**](wm-copydata.md) and displays it to the user.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a><span data-ttu-id="b3117-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3117-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3117-114">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b3117-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b3117-115">**FindWindow**</span><span class="sxs-lookup"><span data-stu-id="b3117-115">**FindWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 