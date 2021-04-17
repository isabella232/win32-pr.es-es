---
description: Proporciona acceso al contexto de un objeto de cadena CAPICOM. Este contexto permite usar la cadena de confianza de certificados de CAPICOM en otras derivaciones de CryptoAPI.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670297"
---
# <a name="ichaincontext-interface"></a>Interfaz IChainContext

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La interfaz **IChainContext** proporciona acceso al contexto de un objeto de [**cadena**](chain.md) CAPICOM. Este contexto permite usar la cadena de confianza de certificados de CAPICOM en otras derivaciones de CryptoAPI.

## <a name="when-to-use"></a>Cuándo se usa

Use esta interfaz cuando necesite usar un objeto de [**cadena**](chain.md) CAPICOM en otra derivación de CryptoAPI.

## <a name="members"></a>Miembros

La interfaz **IChainContext** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IChainContext** tiene estos métodos.



| Método                                           | Descripción                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Libera un \_ contexto de cadena PCCERT \_ adquirido a través de la propiedad [**ChainContext**](ichaincontext-chaincontext.md) .<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IChainContext** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso           | Descripción                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lectura/escritura<br/> | Establece o recupera el \_ \_ contexto de la cadena de PCCERT de un certificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




