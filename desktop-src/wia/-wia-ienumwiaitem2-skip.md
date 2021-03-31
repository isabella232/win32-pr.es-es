---
description: Omite el número especificado de elementos durante una enumeración de objetos IWiaItem2 disponibles.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2:: Skip (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001306"
---
# <a name="ienumwiaitem2skip-method"></a>IEnumWiaItem2:: Skip (método)

Omite el número especificado de elementos durante una enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cElt* \[ de\]
</dt> <dd>

Tipo: **ULong**

Especifica el número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




