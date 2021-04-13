---
title: WM/StreamTypeInfo
description: El atributo WM/StreamTypeInfo contiene la información de configuración para la secuencia especificada en el archivo ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato de Windows Media WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419454"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

El atributo **WM/StreamTypeInfo** contiene la información de configuración para la secuencia especificada en el archivo ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>Tipo de datos

[**WM \_ \_ \_ información de tipo de secuencia**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**tipo WMT \_ \_ binario**)

## <a name="remarks"></a>Observaciones

Este atributo se aplica a flujos específicos. No se puede recuperar este atributo para el flujo 0.

Este atributo es de solo lectura.

El objeto del editor de metadatos puede tener acceso a **WM/StreamTypeInfo** . Esta es la única manera de tener acceso a la información de configuración de la secuencia sin abrir el archivo con el objeto lector (o el objeto lector sincrónico).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




