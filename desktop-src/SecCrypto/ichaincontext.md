---
description: Proporciona acceso al contexto de un objeto de cadena CAPICOM. Este contexto permite usar la cadena de confianza de certificados CAPICOM en otras derivaciones de CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interfaz IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270980"
---
# <a name="ichaincontext-interface"></a>Interfaz IChainContext

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La **interfaz IChainContext** proporciona acceso al contexto de un objeto de cadena CAPICOM. [](chain.md) Este contexto permite usar la cadena de confianza de certificados CAPICOM en otras derivaciones de CryptoAPI.

## <a name="when-to-use"></a>Cuándo se usa

Use esta interfaz cuando necesite usar [](chain.md) un objeto de cadena CAPICOM en otra derivación de CryptoAPI.

## <a name="members"></a>Members

La **interfaz IChainContext** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IChainContext** tiene estos métodos.



| Método                                           | Descripción                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Libera un CONTEXTO DE CADENA DE PCCERT \_ adquirido a través de la propiedad \_ [**ChainContext.**](ichaincontext-chaincontext.md)<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IChainContext** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso           | Descripción                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lectura y escritura<br/> | Establece o recupera el CONTEXTO DE CADENA DE PCCERT \_ \_ de un certificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




