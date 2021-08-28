---
description: Un identificador HRECOGNIZER se usa para crear un contexto de reconocedor, recuperar los atributos y propiedades del reconocedor y determinar qué propiedades de paquete necesita el reconocedor para realizar el reconocimiento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Identificador HRECOGNIZER (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192890991dcb7e8b0a0086bbca68a6ccbc2af790d9c7d78e76fe963d268c8240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092455"
---
# <a name="hrecognizer-handle"></a>Identificador HRECOGNIZER

Un **identificador HRECOGNIZER** se usa para crear un contexto de reconocedor, recuperar los atributos y propiedades del reconocedor y determinar qué propiedades de paquete necesita el reconocedor para realizar el reconocimiento.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Comentarios

Las funciones siguientes usan **un HRECOGNIZER**.



| Función                                                               | Descripción                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Crea un reconocedor.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Destruye un reconocedor.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Devuelve los atributos del reconocedor.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Crea un contexto de reconocedor.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Destruye un contexto de reconocedor.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Obtiene todos los reconocedores.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Recupera una lista de propiedades que el reconocedor puede devolver para un intervalo de resultados.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Recupera una descripción del paquete que contiene las propiedades del paquete que usa el reconocedor.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Recupera los intervalos de puntos Unicode que admite el reconocedor.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Carga los atributos almacenados en caché de un reconocedor.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



 

 




