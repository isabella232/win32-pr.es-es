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
# <a name="working-with-portable-devices"></a><span data-ttu-id="e3da0-111">Trabajar con dispositivos portátiles</span><span class="sxs-lookup"><span data-stu-id="e3da0-111">Working with Portable Devices</span></span>

<span data-ttu-id="e3da0-112">En esta sección se describe cómo usar un control ActiveX de Windows Media Player remoto para trabajar con dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="e3da0-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="e3da0-113">En los ejemplos de código de esta sección se usan las clases Active Template Library (ATL), como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="e3da0-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="e3da0-114">Encabezados incluidos</span><span class="sxs-lookup"><span data-stu-id="e3da0-114">Included Headers</span></span>

<span data-ttu-id="e3da0-115">Para usar el código de esta sección, incluya los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="e3da0-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="e3da0-116">Puntero IWMPPlayer</span><span class="sxs-lookup"><span data-stu-id="e3da0-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="e3da0-117">El puntero **IWMPPlayer** se almacena en una variable miembro.</span><span class="sxs-lookup"><span data-stu-id="e3da0-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="e3da0-118">Los dispositivos se almacenan en una matriz</span><span class="sxs-lookup"><span data-stu-id="e3da0-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="e3da0-119">El código de ejemplo tiene acceso a la siguiente variable miembro, que se va a declarar en el encabezado del proyecto:</span><span class="sxs-lookup"><span data-stu-id="e3da0-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="e3da0-120">El recuento de dispositivos se almacena en una variable miembro.</span><span class="sxs-lookup"><span data-stu-id="e3da0-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="e3da0-121">Recuperación de un puntero de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e3da0-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="e3da0-122">Un puntero a un dispositivo determinado se recupera a través de su índice de matriz mediante código similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="e3da0-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="e3da0-123">Tenga en cuenta que el índice que se muestra en los ejemplos anteriores no es el índice de Asociación para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3da0-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="e3da0-124">Es el índice del dispositivo en la matriz personalizada de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e3da0-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="e3da0-125">Limpieza</span><span class="sxs-lookup"><span data-stu-id="e3da0-125">Cleaning Up</span></span>

<span data-ttu-id="e3da0-126">En los ejemplos se usa la siguiente función para liberar la memoria de la matriz de dispositivos y liberar los punteros de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e3da0-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


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



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="e3da0-127">Los dispositivos se muestran en un cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="e3da0-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="e3da0-128">La función GetSelectedDeviceIndex devuelve el índice del dispositivo seleccionado por el usuario en un cuadro de lista mediante el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e3da0-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="e3da0-129">El estado de la interfaz de usuario se administra mediante una sola función</span><span class="sxs-lookup"><span data-stu-id="e3da0-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="e3da0-130">La función SetUIState administra la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e3da0-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="e3da0-131">Los detalles de esta función no son relevantes para las discusiones de esta sección, pero tenga en cuenta que esta función realiza tareas como habilitar o deshabilitar los controles y cambiar el texto para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e3da0-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="e3da0-132">La enumeración UIState se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e3da0-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="e3da0-133">El parámetro *bConnected* especifica si se va a configurar la interfaz de usuario para un dispositivo conectado (true significa que el dispositivo está conectado).</span><span class="sxs-lookup"><span data-stu-id="e3da0-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="e3da0-134">Los parámetros *NewState* y *bConnected* transmiten la información necesaria para que la función realice su trabajo.</span><span class="sxs-lookup"><span data-stu-id="e3da0-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="e3da0-135">En las secciones siguientes se proporcionan explicaciones del código de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e3da0-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="e3da0-136">Enumerar dispositivos</span><span class="sxs-lookup"><span data-stu-id="e3da0-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="e3da0-137">Recuperación de atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e3da0-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="e3da0-138">Mostrando el progreso de la sincronización</span><span class="sxs-lookup"><span data-stu-id="e3da0-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="e3da0-139">Administrar listas de reproducción de sincronización</span><span class="sxs-lookup"><span data-stu-id="e3da0-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="e3da0-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3da0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3da0-141">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="e3da0-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




