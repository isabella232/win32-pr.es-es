---
title: Modificador /target
description: El modificador/Target permite al compilador MIDL habilitar las optimizaciones disponibles solo en las versiones recientes de Windows. El modificador/Target activa automáticamente modificadores adicionales.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- modificador/Target MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104083522"
---
# <a name="target-switch"></a>Modificador /target

El modificador **/target** permite al compilador MIDL habilitar las optimizaciones disponibles solo en las versiones recientes de Windows. El modificador **/target** activa automáticamente modificadores adicionales.

``` syntax
midl /target level
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*level* 
</dt> <dd>

Especifica el nivel de destino, como NT50, NT51, NT60, NT61, NT62 o NT100.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/target** activa automáticamente modificadores adicionales, según el sistema operativo, como se especifica en la tabla siguiente:



| Sistema operativo | nivel/Target | Conmutadores activados                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf/error All/Robust               |
| Windows XP       | NT51          | /Oicf/error All/Robust/protocolo All |
| Windows Vista    | NT60          | /Oicf/error All/Robust/protocolo All |
| Windows 7        | NT61          | /Oicf/error All/Robust/protocolo All |
| Windows 8        | NT62          | /Oicf/error All/Robust/protocolo All |
| Windows 10       | NT100         | /Oicf/error All/Robust/protocolo All |
 

Para asegurarse de que un código auxiliar se ejecute en el sistema especificado por el modificador **/target** , MIDL emite un error cuando una característica disponible solo en una versión más reciente de Windows está presente. En la tabla siguiente se especifica el nivel mínimo de **/target** necesario para habilitar la característica. Los niveles de destino más altos incluyen todas las características de los niveles de destino inferiores.



| Nivel mínimo necesario de/Target | Características                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /Robust<br/> \[message\]<br/> \[async\]<br/> \[\_UUID asincrónico\]<br/> \[notificar \] en modo/Oicf<br/> \[codificar \] o \[ descodificar \] en modo/Oicf<br/>                   |
| NT51                           | compatibilidad con/protocolo 64 bits<br/> \[\_omitir parcial\]<br/> \[forzar \_ asignación\]<br/>                                                                                                 |
| NT60                           | Serialización de estructura compleja forzada<br/> Identificadores de contexto en una matriz o estructura<br/> \[\]compatibilidad de intervalo para cadenas no de tamaño<br/> \[escribir \_ el \_ identificador de contexto STRICT \_\]<br/> |
| NT61                           | Las llamadas directas de código auxiliar COM para interfaces con menos de 32 métodos requieren la vinculación de códigos auxiliares COM con **OLE32.DLL**.<br/>                                                                          |
| NT62                           | Compatibilidad con ARM<br/> Compatibilidad con WinRT<br/>                                                                                                                                                   |
| NT100                          | \[\]compatibilidad con system_handle<br /> |


 

## <a name="examples"></a>Ejemplos

**MIDL/Target NT50**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
