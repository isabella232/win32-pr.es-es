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
# <a name="using-acf-attributes-in-an-idl-file"></a>Usar atributos ACF en un archivo IDL

Puede usar la opción del compilador de MIDL de [**\_ configuración**](-app-config.md) de la aplicación para especificar los atributos de identificador de enlace en el archivo IDL en lugar de en un archivo ACF independiente. En concreto, puede aplicar los atributos de identificador [**automático \_**](auto-handle.md), identificador [**implícito \_**](implicit-handle.md)y [**\_ identificador explícito**](explicit-handle.md) al encabezado de una interfaz RPC en un archivo IDL. Considere la posibilidad de usar esta opción si la aplicación RPC no requiere otros atributos ACF y, si no necesita compatibilidad estricta con OSF-DCE.

 

 




