---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'IMpeg2PsiParser:: GetTransportStreamId (método)'
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
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677169"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>IMpeg2PsiParser:: GetTransportStreamId (método)

La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.

El `GetTransportStreamId` método recupera el \_ \_ campo de identificador de flujo de transporte de la Pat. Este valor lo define el usuario y se puede usar para distinguir un flujo de transporte determinado de otras secuencias de la misma red. Un flujo de transporte contiene como máximo una PAT.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStreamId* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el campo de identificador de flujo de transporte \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT** . Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Correcto.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Ejemplo de filtro de analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




