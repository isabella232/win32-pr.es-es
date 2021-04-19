---
description: Establece o recupera el \_ \_ contexto de la cadena de PCCERT de un certificado.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'IChainContext:: ChainContext (propiedad)'
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
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690008"
---
# <a name="ichaincontextchaincontext-property"></a>IChainContext:: ChainContext (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La propiedad **ChainContext** establece o recupera el \_ \_ contexto de cadena PCCERT de un certificado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Valor de propiedad

El \_ \_ contexto de la cadena de PCCERT del certificado.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de propiedad **colocan \_ ChainContext** y **Get \_ ChainContext** se ejecutan correctamente, devuelven los valores \_ correctos.

Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Debe llamar al método [**FreeContext**](ichaincontext-freecontext.md) o a la función [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) para liberar el contexto.

Si establece la propiedad **ChainContext** , se restablece el estado del objeto de [**cadena**](chain.md) completo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




