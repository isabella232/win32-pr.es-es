---
title: Uso de la extensión ADSI para Servicios de Escritorio remoto la configuración de usuario
description: La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante el uso de los métodos implementados por la extensión de interfaces de servicio Active Directory (ADSI), que se incluye con la biblioteca de vínculos dinámicos Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, uso de la extensión ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995560"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="4ac63-104">Uso de la extensión ADSI para Servicios de Escritorio remoto la configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="4ac63-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="4ac63-105">La extensión de interfaces de servicios de Active Directory (ADSI) para Servicios de Escritorio remoto configuración de usuario es una biblioteca que se incluye en la biblioteca de vínculos dinámicos Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="4ac63-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="4ac63-106">La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante los métodos implementados por la extensión.</span><span class="sxs-lookup"><span data-stu-id="4ac63-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="4ac63-107">Los métodos permiten la configuración de las propiedades que están disponibles en la interfaz de extensión para Servicios de Escritorio remoto usuarios.</span><span class="sxs-lookup"><span data-stu-id="4ac63-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="4ac63-108">La extensión ADSI para Servicios de Escritorio remoto configuración de usuario admite el examen y la manipulación de Servicios de Escritorio remoto propiedades de usuario almacenadas en la base de datos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="4ac63-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="4ac63-109">La extensión también admite la configuración de las propiedades de usuario que se almacenan en el Active Directory, a través de la API del Protocolo ligero de acceso a directorios (LDAP).</span><span class="sxs-lookup"><span data-stu-id="4ac63-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="4ac63-110">El proveedor implementa los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ac63-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="4ac63-111">[**IADs:: get**](/windows/desktop/api/iads/nf-iads-iads-get).</span><span class="sxs-lookup"><span data-stu-id="4ac63-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="4ac63-112">Este método busca una propiedad concreta o un conjunto de propiedades en una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="4ac63-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="4ac63-113">[**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="4ac63-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="4ac63-114">Este método configura una propiedad concreta o un conjunto de propiedades en una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="4ac63-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="4ac63-115">Consulte la [referencia de la extensión ADSI para servicios de escritorio remoto configuración de usuario](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) para obtener una lista de las propiedades de usuario servicios de escritorio remoto específicas que se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="4ac63-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="4ac63-116">Para obtener más información sobre el acceso y la modificación de atributos con ADSI, vea [obtener acceso a datos y manipularlos con ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span><span class="sxs-lookup"><span data-stu-id="4ac63-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="4ac63-117">Para obtener más información sobre el uso de las convenciones de nomenclatura ADSI y las cadenas AdsPath, consulte la información sobre [proveedores de servicios ADSI](/windows/desktop/ADSI/adsi-system-providers) individuales en la documentación del kit de desarrollo de software (SDK) de las [interfaces de servicio de Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) .</span><span class="sxs-lookup"><span data-stu-id="4ac63-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 