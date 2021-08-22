---
description: Libera un CONTEXTO DE CADENA DE PCCERT \_ adquirido a través de la propiedad \_ ChainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: IChainContext::FreeContext (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 10a6d0576cefd1c28e8f05fe455b89be90dcd36386b4312ef1921511616bce2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005493"
---
# <a name="ichaincontextfreecontext-method"></a>IChainContext::FreeContext (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

El **método FreeContext** libera un CONTEXTO DE CADENA DE PCCERT \_ adquirido a través de la propiedad \_ [**ChainContext.**](ichaincontext-chaincontext.md)

## <a name="syntax"></a>Sintaxis


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pChainContext* \[ En\]
</dt> <dd>

CONTEXTO DE CADENA DE PCCERT \_ que se va a \_ publicar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT**. Un valor de S \_ OK indica que se ha correcto. Cualquier otro valor indica que se ha podido hacer la operación.

## <a name="remarks"></a>Comentarios

Este método no libera el CONTEXTO DE CADENA DE PCCERT \_ incluido dentro de un objeto \_ [**Chain.**](chain.md) Solo se debe usar para liberar un CONTEXTO DE CADENA DE PCCERT \_ adquirido a través de la propiedad \_ [**ChainContext.**](ichaincontext-chaincontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




