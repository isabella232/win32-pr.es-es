---
title: Devoluciones de llamada Bluetooth
description: Las funciones de devolución de llamada de Bluetooth en esta sección se usan en combinación con funciones que permiten administrar dispositivos y servicios Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773650"
---
# <a name="bluetooth-callbacks"></a><span data-ttu-id="a0554-103">Devoluciones de llamada Bluetooth</span><span class="sxs-lookup"><span data-stu-id="a0554-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="a0554-104">Las funciones de devolución de llamada de Bluetooth en esta sección se usan en combinación con funciones que permiten administrar dispositivos y servicios Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="a0554-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="a0554-105">Bluetooth también es compatible con la interfaz de programación de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a0554-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="a0554-106">Para obtener más información acerca de la programación de Bluetooth mediante la interfaz de Windows Sockets, consulte [compatibilidad de Windows Sockets con Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="a0554-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="a0554-107">Sección</span><span class="sxs-lookup"><span data-stu-id="a0554-107">Section</span></span>                                                                                      | <span data-ttu-id="a0554-108">Contenido</span><span class="sxs-lookup"><span data-stu-id="a0554-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0554-109">**devolución de llamada de \_ autenticación pfn \_**</span><span class="sxs-lookup"><span data-stu-id="a0554-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="a0554-110">Se usa junto con la función [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="a0554-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="a0554-111">**\_devolución de llamada de autenticación pfn \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="a0554-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="a0554-112">Se usa junto con la función [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .</span><span class="sxs-lookup"><span data-stu-id="a0554-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="a0554-113">**PFN \_ \_ devolución de \_ llamada de atributos de enumeración Bluetooth \_**</span><span class="sxs-lookup"><span data-stu-id="a0554-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="a0554-114">Se le llama una vez para cada atributo que se encuentra en el parámetro *pSDPStream* que se pasa a la llamada a la función [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) .</span><span class="sxs-lookup"><span data-stu-id="a0554-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="a0554-115">**devolución de llamada de \_ dispositivo pfn \_**</span><span class="sxs-lookup"><span data-stu-id="a0554-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="a0554-116">Se usa en asociación con la selección de dispositivos Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="a0554-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 




