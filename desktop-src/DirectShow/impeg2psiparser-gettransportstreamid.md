---
description: 'Método IMpeg2PsiParser::GetTransportStreamId: la implementación de este método se proporciona como código de ejemplo con el SDK DirectShow. No se admite DirectShow API.'
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: IMpeg2PsiParser::GetTransportStreamId (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: e78eabce23633029e4ef3dfe6c6777c586a5d74ed28ccfe466c89064851f8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791905"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>IMpeg2PsiParser::GetTransportStreamId (método)

La implementación de este método se proporciona como código de ejemplo con DirectShow SDK. No se admite DirectShow API.

El `GetTransportStreamId` método recupera el campo de identificador de flujo de transporte del \_ \_ PAT. El usuario define este valor y se puede usar para distinguir una secuencia de transporte determinada de otras secuencias de la misma red. Una secuencia de transporte contiene como máximo un PAT.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStreamId* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el campo de identificador \_ de flujo \_ de transporte.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT.** Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Correcto.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMpeg2PsiParser (interfaz)**](impeg2psiparser.md)
</dt> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




