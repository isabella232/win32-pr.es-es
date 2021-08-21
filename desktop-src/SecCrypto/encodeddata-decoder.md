---
description: Obtiene un objeto descodificador, si existe uno.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Método EncodedData.Decoder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7496aa3873fda9e4cd0adc86773a8c06ca60be25e3625c26f3b7a97508f48e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766828"
---
# <a name="encodeddatadecoder-method"></a>Método EncodedData.Decoder

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase AsnEncodedData en**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Decoder** obtiene un objeto descodificador, si existe uno.

## <a name="syntax"></a>Sintaxis


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Comentarios

Si los datos codificados no tienen un objeto descodificador, **se devuelve NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
