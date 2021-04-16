---
description: Un protocolo de transporte debe estar instalado correctamente en el sistema y estar registrado en Windows Sockets para ser accesible para una aplicación.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Acceso simultáneo a varios protocolos de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706103"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="3654e-103">Acceso simultáneo a varios protocolos de transporte</span><span class="sxs-lookup"><span data-stu-id="3654e-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="3654e-104">Un protocolo de transporte debe estar instalado correctamente en el sistema y estar registrado en Windows Sockets para ser accesible para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3654e-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="3654e-105">La \_ biblioteca32.dll de Ws2 exporta un conjunto de funciones para facilitar el proceso de registro.</span><span class="sxs-lookup"><span data-stu-id="3654e-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="3654e-106">Esto incluye la creación de un nuevo registro y la eliminación de uno existente.</span><span class="sxs-lookup"><span data-stu-id="3654e-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="3654e-107">Cuando se crean nuevos registros, el autor de la llamada (es decir, el script de instalación del proveedor de la pila) proporciona una o varias estructuras de información de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) rellenadas que contienen un conjunto completo de información sobre el protocolo.</span><span class="sxs-lookup"><span data-stu-id="3654e-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="3654e-108">Para obtener más información, vea [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span><span class="sxs-lookup"><span data-stu-id="3654e-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="3654e-109">Cualquier pila de transporte instalada de esta manera se conoce como proveedor de servicios de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="3654e-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="3654e-110">En Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) y Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3654e-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="3654e-111">el catálogo Winsock que contiene una lista de proveedores de transporte y de espacio de nombres instalados se puede mostrar en un símbolo del sistema con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="3654e-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="3654e-112">**netsh winsock show Catalog**</span><span class="sxs-lookup"><span data-stu-id="3654e-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="3654e-113">El kit de desarrollo de software (SDK) de Microsoft Windows incluye *Sporder.exe*, que permite al usuario ver y modificar el orden en el que se enumeran los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="3654e-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="3654e-114">Con *Sporder.exe*, un usuario puede establecer manualmente una pila de protocolo TCP/IP determinada como el proveedor TCP/IP predeterminado si hay más de una pila de este tipo.</span><span class="sxs-lookup"><span data-stu-id="3654e-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="3654e-115">La aplicación *Sporder.exe* utiliza funciones exportadas de *Sporder.dll* para reordenar los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="3654e-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="3654e-116">Como resultado, las aplicaciones de instalación pueden utilizar la interfaz proporcionada por *Sporder.dll* para reordenar los proveedores de servicios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3654e-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="3654e-117">Protocolos en capas y cadenas de protocolo</span><span class="sxs-lookup"><span data-stu-id="3654e-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="3654e-118">Usar varios protocolos</span><span class="sxs-lookup"><span data-stu-id="3654e-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="3654e-119">Varias restricciones de proveedor en Select</span><span class="sxs-lookup"><span data-stu-id="3654e-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 
