---
description: Un identificador HRECOGNIZER se usa para crear un contexto de reconocedor, recuperar los atributos y propiedades del reconocedor, y determinar qué propiedades de paquete requiere el reconocedor para realizar el reconocimiento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Identificador de HRECOGNIZER (Resumen. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360348"
---
# <a name="hrecognizer-handle"></a>Identificador de HRECOGNIZER

Un identificador **HRECOGNIZER** se usa para crear un contexto de reconocedor, recuperar los atributos y propiedades del reconocedor, y determinar qué propiedades de paquete requiere el reconocedor para realizar el reconocimiento.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Observaciones

Las siguientes funciones usan un **HRECOGNIZER**.



| Función                                                               | Descripción                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Crea un reconocedor.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Destruye un reconocedor.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Devuelve los atributos del reconocedor.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Crea un contexto de reconocedor.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Destruye un contexto de reconocedor.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Obtiene todos los reconocedores.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Recupera una lista de propiedades que el reconocedor puede devolver para un intervalo de resultados.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Recupera una descripción de paquete que contiene las propiedades de paquete que utiliza el reconocedor.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Recupera los intervalos de puntos Unicode que admite el reconocedor.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Carga los atributos almacenados en memoria caché de un reconocedor.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Resumen. h</dt> </dl> |



 

 




