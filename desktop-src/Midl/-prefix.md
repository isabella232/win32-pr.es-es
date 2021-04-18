---
title: modificador/prefix
description: El modificador/prefix indica al compilador de MIDL que agregue cadenas de prefijo a los nombres de rutina de código auxiliar de cliente o servidor.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix modificador MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532739"
---
# <a name="prefix-switch"></a>modificador/prefix

El modificador **/prefix** indica al compilador de MIDL que agregue cadenas de prefijo a los nombres de rutina de código auxiliar de cliente o servidor. Se puede usar para permitir que un único programa sea un cliente y un servidor de la misma interfaz, sin que los nombres de las rutinas del cliente y del servidor entren en conflicto entre sí.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>cliente * * * *


</dt> <dd>

Afecta únicamente a los nombres de rutina de código auxiliar de cliente.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub****


</dt> <dd>

Igual que el *cliente*. Afecta únicamente a los nombres de rutina de código auxiliar de cliente.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>servidor * * * *


</dt> <dd>

Afecta únicamente a los nombres de rutinas a los que llama la rutina de código auxiliar del servidor.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub****


</dt> <dd>

Igual que el *servidor*. Afecta únicamente a los nombres de rutinas a los que llama la rutina de código auxiliar del servidor.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>cambiar * * * *


</dt> <dd>

Afecta a un prototipo adicional agregado al archivo de encabezado.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>todo * * * *


</dt> <dd>

Afecta a los nombres de rutina de código auxiliar de cliente y servidor.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Si el prefijo de las rutinas del lado cliente es diferente del prefijo para las rutinas del lado servidor, el archivo de encabezado generado tendrá tanto prototipos de rutina del lado cliente como prototipos de rutina del lado servidor.

El modificador **/prefix** resulta útil cuando se utiliza un único archivo de encabezado con códigos auxiliares de varias ejecuciones del compilador de MIDL. Esto fuerza los prototipos de rutina adicionales en el archivo de encabezado.

En todos los casos, el cliente, el servidor y los prefijos de conmutador invalidarán un prefijo ALL.

## <a name="examples"></a>Ejemplos

**cliente de/Prefix de MIDL "c \_ " Server "s \_ "**

**MIDL/prefix All "Moo \_ "**

**cliente de/prefix MIDL "corteza \_ "**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




