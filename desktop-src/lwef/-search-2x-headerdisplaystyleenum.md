---
title: Enumeración HeaderDisplayStyle
description: Usado por IResultsViewer HeaderStyle para establecer o devolver el estilo de encabezado actual.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Enumeración HeaderDisplayStyle características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699676"
---
# <a name="headerdisplaystyle-enumeration"></a>Enumeración HeaderDisplayStyle

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Usado por [**IResultsViewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) para establecer o devolver el estilo de encabezado actual.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**
</dt> <dd>

Indica o establece el uso de encabezados completos.

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**
</dt> <dd>

Indica o establece el uso de encabezados de compactación.

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noheader**
</dt> <dd>

Indica o establece el uso de ningún encabezado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





