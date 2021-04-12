---
title: Trabajar con dispositivos portátiles
description: Trabajar con dispositivos portátiles
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, dispositivos portátiles
- Modelo de objetos de Windows Media Player, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Control ActiveX de Windows Media Player, dispositivos portátiles
- Control ActiveX, dispositivos portátiles
- Control ActiveX móvil de Windows Media Player, dispositivos portátiles
- Windows Media Player dispositivos móviles y portátiles
- dispositivos portátiles, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357698"
---
# <a name="working-with-portable-devices"></a>Trabajar con dispositivos portátiles

En esta sección se describe cómo usar un control ActiveX de Windows Media Player remoto para trabajar con dispositivos portátiles.

En los ejemplos de código de esta sección se usan las clases Active Template Library (ATL), como **CComPtr**.

## <a name="included-headers"></a>Encabezados incluidos

Para usar el código de esta sección, incluya los encabezados siguientes:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>Puntero IWMPPlayer

El puntero **IWMPPlayer** se almacena en una variable miembro.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Los dispositivos se almacenan en una matriz

El código de ejemplo tiene acceso a la siguiente variable miembro, que se va a declarar en el encabezado del proyecto:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



El recuento de dispositivos se almacena en una variable miembro.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Recuperación de un puntero de dispositivo

Un puntero a un dispositivo determinado se recupera a través de su índice de matriz mediante código similar al siguiente:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Tenga en cuenta que el índice que se muestra en los ejemplos anteriores no es el índice de Asociación para el dispositivo. Es el índice del dispositivo en la matriz personalizada de dispositivos.

## <a name="cleaning-up"></a>Limpieza

En los ejemplos se usa la siguiente función para liberar la memoria de la matriz de dispositivos y liberar los punteros de interfaz:


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a>Los dispositivos se muestran en un cuadro de lista

La función GetSelectedDeviceIndex devuelve el índice del dispositivo seleccionado por el usuario en un cuadro de lista mediante el código siguiente:


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>El estado de la interfaz de usuario se administra mediante una sola función

La función SetUIState administra la interfaz de usuario.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Los detalles de esta función no son relevantes para las discusiones de esta sección, pero tenga en cuenta que esta función realiza tareas como habilitar o deshabilitar los controles y cambiar el texto para mostrar en la interfaz de usuario.

La enumeración UIState se definió de la siguiente manera:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



El parámetro *bConnected* especifica si se va a configurar la interfaz de usuario para un dispositivo conectado (true significa que el dispositivo está conectado). Los parámetros *NewState* y *bConnected* transmiten la información necesaria para que la función realice su trabajo.

En las secciones siguientes se proporcionan explicaciones del código de ejemplo:

-   [Enumerar dispositivos](enumerating-devices.md)
-   [Recuperación de atributos de dispositivo](retrieving-device-attributes.md)
-   [Mostrando el progreso de la sincronización](showing-synchronization-progress.md)
-   [Administrar listas de reproducción de sincronización](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control del reproductor**](player-control-guide.md)
</dt> </dl>

 

 




