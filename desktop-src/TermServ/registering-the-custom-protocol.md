---
title: Registro del administrador de protocolos
description: Debe crear al menos una entrada de valor de registro para el administrador de protocolos para que el servicio de Servicios de Escritorio remoto pueda crear una instancia de ella.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418522"
---
# <a name="registering-the-protocol-manager"></a><span data-ttu-id="e012a-103">Registro del administrador de protocolos</span><span class="sxs-lookup"><span data-stu-id="e012a-103">Registering the Protocol Manager</span></span>

<span data-ttu-id="e012a-104">Debe crear al menos una entrada de valor de registro para el administrador de protocolos para que el servicio de Servicios de Escritorio remoto pueda crear una instancia de ella.</span><span class="sxs-lookup"><span data-stu-id="e012a-104">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

## <a name="registry-location"></a><span data-ttu-id="e012a-105">Ubicación del registro</span><span class="sxs-lookup"><span data-stu-id="e012a-105">Registry Location</span></span>

<span data-ttu-id="e012a-106">Cree una clave del registro en la siguiente ubicación para cada agente de escucha ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que usa el protocolo.</span><span class="sxs-lookup"><span data-stu-id="e012a-106">Create a registry key in the following location for each listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) that your protocol uses.</span></span> <span data-ttu-id="e012a-107">En este ejemplo, las nuevas claves de agente de escucha se denominan *MyListener1* y *MyListener2*.</span><span class="sxs-lookup"><span data-stu-id="e012a-107">In this example, the new listener keys are called *MyListener1* and *MyListener2*.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

<span data-ttu-id="e012a-108">Como referencia, puede ver las entradas de valor en la clave de escucha **RDP-TCP** predeterminada en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="e012a-108">For reference, you can view the value entries under the default **RDP-Tcp** listener key in this location.</span></span>

## <a name="registry-value-entries"></a><span data-ttu-id="e012a-109">Entradas de valores del registro</span><span class="sxs-lookup"><span data-stu-id="e012a-109">Registry Value Entries</span></span>

<span data-ttu-id="e012a-110">La clave del agente de escucha para el protocolo debe tener una entrada de valor denominada **\_ objeto LoadableProtocol**</span><span class="sxs-lookup"><span data-stu-id="e012a-110">The listener key for the protocol must have a value entry called **LoadableProtocol\_Object**</span></span><dl> <dt>

<span data-ttu-id="e012a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e012a-111">Data type</span></span>
</dt> <dd><span data-ttu-id="e012a-112">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e012a-112">REG_SZ</span></span></dd> <span data-ttu-id="e012a-113">Interfaz </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> ). El servicio Servicios de Escritorio remoto usa este CLSID para crear una instancia del administrador de protocolos para este agente de escucha después de encontrar el agente de escucha en el registro.</span><span class="sxs-lookup"><span data-stu-id="e012a-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> interface.) The Remote Desktop Services service uses this CLSID to instantiate the protocol manager for this listener after it finds the listener in the registry.</span></span>

<span data-ttu-id="e012a-114">Si el proveedor de protocolo usa más de un agente de escucha, el servicio Servicios de Escritorio remoto solo crea una instancia del administrador de protocolos y la usa para llamar a [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) una vez para cada agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="e012a-114">If your protocol provider uses more than one listener, the Remote Desktop Services service only creates one instance of the protocol manager, and uses it to call [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) once for each listener.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e012a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e012a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e012a-116">Creación de un proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="e012a-116">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="e012a-117">Secuencia de llamada al método</span><span class="sxs-lookup"><span data-stu-id="e012a-117">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> </dl>

 

 




