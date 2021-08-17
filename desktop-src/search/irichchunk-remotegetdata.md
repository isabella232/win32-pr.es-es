---
description: Recupera la propiedad PROPVARIANT y la cadena de entrada que representa un fragmento de datos. Llamar a este método es lo mismo que llamar a GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: IRichChunk::RemoteGetData (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: caaa4ab9688ab8169bd0955c8abb1e976e7eb318e94875be1486e61b32e13207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862803"
---
# <a name="irichchunkremotegetdata-method"></a>IRichChunk::RemoteGetData (método)

Recupera la propiedad [PROPVARIANT y](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) la cadena de entrada que representa un fragmento de datos. Llamar a este método es lo mismo que llamar [**a GetData.**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFirstPos* \[ out\]
</dt> <dd>

Recibe la posición inicial de base cero del intervalo. Este parámetro puede ser **NULL**.

</dd> <dt>

*pLength* \[ out\]
</dt> <dd>

Recibe la longitud del intervalo. Este parámetro puede ser **NULL**.

</dd> <dt>

*ppsz* \[ out\]
</dt> <dd>

Recibe el valor de cadena Unicode asociado o **NULL** si no está disponible.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Recibe el valor [PROPVARIANT asociado](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) o **VT \_ EMPTY** si no está disponible. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
