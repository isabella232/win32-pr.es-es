---
description: Establece o recupera el CONTEXTO DE CADENA DE PCCERT \_ \_ de un certificado.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: Propiedad IChainContext::ChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d5e7bc92aa798766538af19cae440542705a859040aed7fc8d9510e3724051f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005503"
---
# <a name="ichaincontextchaincontext-property"></a>Propiedad IChainContext::ChainContext

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La **propiedad ChainContext** establece o recupera el CONTEXTO DE CADENA DE PCCERT \_ de un \_ certificado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Valor de propiedad

CONTEXTO DE CADENA DE PCCERT \_ \_ del certificado.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de **propiedad \_ ponen ChainContext** **y \_ obtienen ChainContext** correctamente, devuelven S \_ OK.

Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Comentarios

Debe llamar al método [**FreeContext**](ichaincontext-freecontext.md) o a la [**función CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) para liberar el contexto.

Si establece la **propiedad ChainContext,** se restablece el estado de todo el [**objeto Chain.**](chain.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




