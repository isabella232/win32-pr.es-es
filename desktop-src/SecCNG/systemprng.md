---
description: Recupera un número especificado de bytes aleatorios del generador de números aleatorios del sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng función)
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
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666425"
---
# <a name="systemprng-function"></a>SystemPrng función)

\[**SystemPrng** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

La función **SystemPrng** recupera un número especificado de bytes aleatorios del generador de números aleatorios del sistema.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbRandomData* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe los bytes recuperados.

</dd> <dt>

*cbRandomData* \[ de\]
</dt> <dd>

El número de bytes que se van a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio con SP1 de Windows Vista \[\]<br/>                                                                                                                                                                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                                                                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Ksecdd.sys en Windows Server 2008 y Windows Vista con SP1; </dt> <dt>Cng.sys en Windows 7 y Windows Server 2008 R2</dt> </dl> |



 

 




