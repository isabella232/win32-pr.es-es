---
description: Recupera el PROPVARIANT y la cadena de entrada que representa un fragmento de datos. Llamar a este método es igual que llamar a GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'IRichChunk:: RemoteGetData (método)'
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
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153940"
---
# <a name="irichchunkremotegetdata-method"></a>IRichChunk:: RemoteGetData (método)

Recupera el [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) y la cadena de entrada que representa un fragmento de datos. Llamar a este método es igual que llamar a [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

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

*pFirstPos* \[ enuncia\]
</dt> <dd>

Recibe la posición inicial de base cero del intervalo. Este parámetro puede ser **NULL**.

</dd> <dt>

*plength* \[ enuncia\]
</dt> <dd>

Recibe la longitud del intervalo. Este parámetro puede ser **NULL**.

</dd> <dt>

*ppsz* \[ enuncia\]
</dt> <dd>

Recibe el valor de cadena Unicode asociado o **null** si no está disponible.

</dd> <dt>

*pValue* \[ enuncia\]
</dt> <dd>

Recibe el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) asociado o **VT \_ vacío** si no está disponible. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
