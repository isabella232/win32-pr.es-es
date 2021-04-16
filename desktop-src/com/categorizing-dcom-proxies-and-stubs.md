---
title: Categorización de proxies y códigos auxiliares de DCOM
description: Categorización de proxies y códigos auxiliares de DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714479"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="77356-103">Categorización de proxies y códigos auxiliares de DCOM</span><span class="sxs-lookup"><span data-stu-id="77356-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="77356-104">DCOM calcula las referencias a los objetos mediante la construcción de OBJREFs que contienen CLSID.</span><span class="sxs-lookup"><span data-stu-id="77356-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="77356-105">Estos CLSID son vulnerables a los ataques de seguridad porque se pueden cargar archivos dll arbitrarios durante el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="77356-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="77356-106">Sin embargo, \_ \_ \_ se puede especificar la marca de serialización no personalizada EOAC al llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (consulte [**capacidades de \_ autenticación \_ de Eole**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span><span class="sxs-lookup"><span data-stu-id="77356-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="77356-107">La configuración de esta marca ayuda a proteger la seguridad del servidor al usar DCOM porque reduce las posibilidades de ejecutar archivos dll arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="77356-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="77356-108">Cuando se establece esta marca, el servidor permite el cálculo de referencias solo de los CLSID que se implementan en ole32.dll, comadmin.dll, comsvcs.dll o es.dll, o que implementan el \_ identificador de categoría del contador de referencias CATID.</span><span class="sxs-lookup"><span data-stu-id="77356-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="77356-109">\_El contador de referencias CATID es un GUID de categoría de componente que se puede asociar a un CLSID que se va a serializar.</span><span class="sxs-lookup"><span data-stu-id="77356-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="77356-110">Las interfaces a las que se calculan las referencias personalizadas con este CLSID se permiten cuando EOAC \_ no \_ \_ se establece ningún cálculo de referencias personalizado a través de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="77356-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77356-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77356-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77356-112">Categorías del componente</span><span class="sxs-lookup"><span data-stu-id="77356-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 