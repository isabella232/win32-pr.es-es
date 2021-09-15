---
title: Trabajar con dispositivos portátiles
description: Trabajar con dispositivos portátiles
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Reproductor de Windows Media dispositivos portátiles
- Reproductor de Windows Media modelo de objetos, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Reproductor de Windows Media ActiveX control, dispositivos portátiles
- ActiveX control, dispositivos portátiles
- Reproductor de Windows Media Control de ActiveX móviles, dispositivos portátiles
- Reproductor de Windows Media Dispositivos móviles y portátiles
- dispositivos portátiles, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467338"
---
# <a name="working-with-portable-devices"></a>Trabajar con dispositivos portátiles

En esta sección se describe cómo usar un control Reproductor de Windows Media ActiveX remoto para trabajar con dispositivos portátiles.

Los ejemplos de código de esta sección usan Active Template Library (ATL), como **CComPtr**.

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

El **puntero IWMPPlayer** se almacena en una variable miembro.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Los dispositivos se almacenan en una matriz

El código de ejemplo tiene acceso a la siguiente variable miembro, que se va a declarar en el encabezado del proyecto:


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



El número de dispositivos se almacena en una variable miembro.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Recuperar un puntero de dispositivo

Un puntero a un dispositivo determinado se recupera a través de su índice de matriz mediante código similar al siguiente:


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Tenga en cuenta que el índice que se muestra en los ejemplos anteriores no es el índice de asociación del dispositivo. Es el índice del dispositivo en la matriz personalizada de dispositivos.

## <a name="cleaning-up"></a>Limpieza

En los ejemplos se usa la siguiente función para liberar la memoria en la matriz de dispositivos y para liberar los punteros de interfaz:


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



## <a name="user-interface-state-is-managed-by-a-single-function"></a>Interfaz de usuario estado se administra mediante una sola función

La función SetUIState administra la interfaz de usuario.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Los detalles de esta función no son pertinentes para las discusiones de esta sección, pero tenga en cuenta que esta función realiza tareas como habilitar o deshabilitar controles y cambiar el texto de presentación en la interfaz de usuario.

La enumeración UIState se definió de la siguiente manera:


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



El *parámetro bConnected* especifica si se debe configurar la interfaz de usuario para un dispositivo conectado (TRUE significa que el dispositivo está conectado). Los *parámetros NewState* *y bConnected* transmiten la información necesaria para que la función realice su trabajo.

En las secciones siguientes se proporcionan explicaciones del código de ejemplo:

-   [Enumeración de dispositivos](enumerating-devices.md)
-   [Recuperación de atributos de dispositivo](retrieving-device-attributes.md)
-   [Mostrar el progreso de la sincronización](showing-synchronization-progress.md)
-   [Administración de listas de reproducción de sincronización](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de control de reproductor**](player-control-guide.md)
</dt> </dl>

 

 




