---
title: WM/StreamTypeInfo
description: El atributo WM/StreamTypeInfo contiene la información de configuración de la secuencia especificada en el archivo ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato multimedia de Windows WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb40926d5ecba3aea2c7f2db64850152c66a25861d4422fddf04670c76d8148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698277"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

El **atributo WM/StreamTypeInfo** contiene la información de configuración de la secuencia especificada en el archivo ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>Tipo de datos

[**WM \_ STREAM \_ TYPE \_ INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT TYPE \_ \_ BINARY**)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a secuencias específicas. No se puede recuperar este atributo para el flujo 0.

Este atributo es de solo lectura.

El objeto del editor de metadatos puede acceder a **WM/StreamTypeInfo.** Esta es la única manera de acceder a la información de configuración de la secuencia sin abrir el archivo con el objeto de lector (o el objeto de lector sincrónico).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




