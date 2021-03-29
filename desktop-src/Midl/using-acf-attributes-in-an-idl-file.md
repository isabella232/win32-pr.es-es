---
title: Usar atributos ACF en un archivo IDL
description: Puede usar la \_ opción del compilador de MIDL/App config para especificar los atributos de identificador de enlace en el archivo IDL en lugar de en un archivo ACF independiente.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL, atributos, uso de ACF en IDL
- MIDL para IDL, usar ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dde95201bc2c729ac126b35e04919fd196cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775349"
---
# <a name="using-acf-attributes-in-an-idl-file"></a><span data-ttu-id="84ab2-105">Usar atributos ACF en un archivo IDL</span><span class="sxs-lookup"><span data-stu-id="84ab2-105">Using ACF Attributes in an IDL File</span></span>

<span data-ttu-id="84ab2-106">Puede usar la opción del compilador de MIDL de [**\_ configuración**](-app-config.md) de la aplicación para especificar los atributos de identificador de enlace en el archivo IDL en lugar de en un archivo ACF independiente.</span><span class="sxs-lookup"><span data-stu-id="84ab2-106">You can use the /[**app\_config**](-app-config.md) MIDL compiler option to specify binding handle attributes in the IDL file rather than in a separate ACF file.</span></span> <span data-ttu-id="84ab2-107">En concreto, puede aplicar los atributos de identificador [**automático \_**](auto-handle.md), identificador [**implícito \_**](implicit-handle.md)y [**\_ identificador explícito**](explicit-handle.md) al encabezado de una interfaz RPC en un archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="84ab2-107">Specifically, you can apply the [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), and [**explicit\_handle**](explicit-handle.md) attributes to the header of an RPC interface in an IDL file.</span></span> <span data-ttu-id="84ab2-108">Considere la posibilidad de usar esta opción si la aplicación RPC no requiere otros atributos ACF y, si no necesita compatibilidad estricta con OSF-DCE.</span><span class="sxs-lookup"><span data-stu-id="84ab2-108">Consider using this option if your RPC application does not require other ACF attributes, and if you do not require strict OSF-DCE compatibility.</span></span>

 

 




