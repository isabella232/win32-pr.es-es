---
description: Recupera un número especificado de bytes aleatorios del generador de números aleatorios del sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Función SystemPrng
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: eae1a46b43278c836ff6ce318dfdce7302bb0e052664a7326f9043a60eec72d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905634"
---
# <a name="systemprng-function"></a>Función SystemPrng

\[**SystemPrng** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [**use BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

La **función SystemPrng** recupera un número especificado de bytes aleatorios del generador de números aleatorios del sistema.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbRandomData* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe los bytes recuperados.

</dd> <dt>

*cbRandomData* \[ En\]
</dt> <dd>

El número de bytes que se van a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista solo con aplicaciones de \[ escritorio sp1\]<br/>                                                                                                                                                                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                                                                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Ksecdd.sys en Windows Server 2008 y Windows Vista con SP1;</dt> <dt>Cng.sys en Windows 7 y Windows Server 2008 R2</dt> </dl> |



 

 




