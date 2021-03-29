---
title: Instalación de EAP
description: Los proveedores implementan EAPs, también conocidos como protocolos de autenticación, en bibliotecas de vínculos dinámicos (dll).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420027"
---
# <a name="eap-installation"></a><span data-ttu-id="2583f-103">Instalación de EAP</span><span class="sxs-lookup"><span data-stu-id="2583f-103">EAP Installation</span></span>

<span data-ttu-id="2583f-104">Los proveedores implementan EAPs, también conocidos como protocolos de autenticación, en bibliotecas de vínculos dinámicos (dll).</span><span class="sxs-lookup"><span data-stu-id="2583f-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="2583f-105">Un archivo DLL para el protocolo de autenticación debe residir en los equipos cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="2583f-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="2583f-106">Para simplificar, los archivos dll de cliente y servidor pueden ser idénticos; sin embargo, esto no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="2583f-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="2583f-107">Además, tenga en cuenta que el mismo archivo DLL puede admitir más de un protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="2583f-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="2583f-108">El proveedor debe proporcionar el software de instalación para instalar y quitar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2583f-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="2583f-109">El software de instalación también debe crear las claves y los valores adecuados para el protocolo de autenticación en el registro del sistema y quitarlos tras la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="2583f-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="2583f-110">La instalación de cada archivo DLL de EAP debe crear la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="2583f-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="2583f-111">**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **servicios** \\ **rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**</span><span class="sxs-lookup"><span data-stu-id="2583f-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="2583f-112">En la ruta de acceso anterior, **&lt; eaptypeid &gt;** es el identificador del Protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="2583f-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="2583f-113">El proveedor debe obtener este identificador de la autoridad de asignación de números de Internet (IANA).</span><span class="sxs-lookup"><span data-stu-id="2583f-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="2583f-114">Para obtener más información y una descripción de los valores admitidos para esta clave, consulte [valores del registro del Protocolo de autenticación](authentication-protocol-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="2583f-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




