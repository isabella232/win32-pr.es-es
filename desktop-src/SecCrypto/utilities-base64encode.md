---
description: Codifica una cadena como Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Utilities. Base64Encode (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690261"
---
# <a name="utilitiesbase64encode-method"></a>Utilities. Base64Encode (método)

\[El método **Base64Encode** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El método **Base64Encode** codifica una cadena como Base64.

## <a name="syntax"></a>Sintaxis


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SrcString* \[ de\]
</dt> <dd>

Cadena que se va a codificar como Base64.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena codificada en Base64.

## <a name="remarks"></a>Observaciones

La codificación Base64 es el esquema que se usa para transmitir datos binarios. Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados. La codificación Base64 a veces se conoce como codificación de 3 a 4. Cada 6 bits del grupo de 24 bits se utiliza como índice en una tabla de asignación (el alfabeto Base64) para obtener un carácter para los datos codificados. Los datos codificados tienen longitudes de línea que están limitadas a 76 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sectores públicos**](utilities.md)
</dt> </dl>

 

 




