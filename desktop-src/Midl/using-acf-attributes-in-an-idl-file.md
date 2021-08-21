---
title: Uso de atributos ACF en un archivo IDL
description: Puede usar la opción del compilador MIDL /app config para especificar atributos de identificador de enlace en el archivo IDL en lugar de \_ en un archivo ACF independiente.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL, atributos, mediante ACF en IDL
- IDL MIDL , mediante ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105525"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Uso de atributos ACF en un archivo IDL

Puede usar la opción del compilador MIDL /[**app \_ config**](-app-config.md) para especificar atributos de identificador de enlace en el archivo IDL en lugar de en un archivo ACF independiente. En concreto, puede aplicar el identificador automático [**, \_**](auto-handle.md) [**el \_**](implicit-handle.md)identificador implícito y los atributos de identificador explícito al encabezado de una interfaz RPC en un archivo IDL. [**\_**](explicit-handle.md) Considere la posibilidad de usar esta opción si la aplicación RPC no requiere otros atributos de ACF y si no requiere compatibilidad estricta con OSF-DCE.

 

 




