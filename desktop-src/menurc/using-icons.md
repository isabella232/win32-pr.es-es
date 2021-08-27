---
title: Usar iconos
description: En esta sección se proporcionan ejemplos de código que muestran cómo realizar tareas relacionadas con iconos.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- resources,icons
- icons,creating
- iconos, mostrar
- iconos, recursos compartidos
- crear iconos
- mostrar iconos
- recursos del icono de uso compartido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db7a5828c80dc27780ac54e4110e37a80f44938c9475904ce32089be50d84f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472603"
---
# <a name="using-icons"></a>Usar iconos

En los temas siguientes se describe cómo realizar ciertas tareas relacionadas con iconos:

-   [Crear un icono](#creating-an-icon)
-   [Mostrar un icono](#displaying-an-icon)
-   [Recursos del icono de uso compartido](#sharing-icon-resources)

## <a name="creating-an-icon"></a>Crear un icono

Para usar un icono, la aplicación debe obtener un identificador para el icono. En el ejemplo siguiente se muestra cómo crear dos identificadores de icono diferentes: uno para el icono de pregunta estándar y otro para un icono personalizado incluido como un recurso en el archivo de definición de recursos de la aplicación.


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



Una aplicación debe implementar iconos personalizados como recursos y debe usar la función [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage,**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) en lugar de crear los iconos en tiempo de ejecución. Este enfoque evita la dependencia de dispositivos, simplifica la localización y permite que las aplicaciones compartan mapas de bits de iconos. Sin embargo, en el ejemplo siguiente se [**usa CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) para crear un icono personalizado en tiempo de ejecución, basado en máscaras de bits de mapa de bits; se incluye para ilustrar cómo el sistema interpreta las máscaras de bits de mapa de bits de icono.


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



Para crear el icono, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) aplica la siguiente tabla truth a las máscaras de bits AND y XOR.



| Máscara de bits AND | Máscara de bits XOR | Mostrar        |
|-------------|-------------|----------------|
| 0           | 0           | Negro          |
| 0           | 1           | Blanco          |
| 1           | 0           | Screen         |
| 1           | 1           | Pantalla inversa |



 

Antes de cerrar, la aplicación debe usar [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) para destruir cualquier icono que haya creado mediante [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect). No es necesario destruir los iconos creados por otras funciones.

## <a name="displaying-an-icon"></a>Mostrar un icono

La aplicación puede cargar y crear iconos para mostrar en el área cliente de la aplicación o en las ventanas secundarias. En el ejemplo siguiente se muestra cómo dibujar un icono en el área cliente de la ventana cuyo contexto de dispositivo (DC) se identifica mediante el *parámetro hdc.*


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



El sistema muestra automáticamente los iconos de clase de una ventana. La aplicación puede asignar iconos de clase al registrar una clase de ventana. La aplicación puede reemplazar un icono de clase mediante la [**función SetClassLong.**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) Esta función cambia la configuración de ventana predeterminada para todas las ventanas de una clase determinada. En el ejemplo siguiente se reemplaza un icono de clase por el icono cuyo identificador de recurso es 480.


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



Para obtener más información sobre las clases de ventana, vea [Clases de ventana](/windows/desktop/winmsg/window-classes).

## <a name="sharing-icon-resources"></a>Recursos del icono de uso compartido

El código siguiente usa las funciones [**CreateIconFromResourceEx,**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)y [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)y varias de las funciones de recursos para crear un identificador de icono basado en datos de icono de otro archivo ejecutable. A continuación, muestra el icono en una ventana.

**Advertencia de seguridad:** El [**uso incorrecto de LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación al cargar el archivo DLL incorrecto. Consulte la documentación **de LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
