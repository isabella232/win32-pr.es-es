---
description: Las \_ constantes de marcador de bits PHONEPRIVILEGE describen las distintas formas en que se puede abrir un dispositivo de teléfono.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Constantes de PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691108"
---
# <a name="phoneprivilege_-constants"></a>Constantes de PHONEPRIVILEGE \_

Las constantes de marcador de bits **PHONEPRIVILEGE \_** describen las distintas formas en que se puede abrir un dispositivo de teléfono.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**MONITOR de PHONEPRIVILEGE \_**
</dt> <dd> <dl> <dt>



Una aplicación que abre un dispositivo telefónico con el privilegio monitor está informado sobre los eventos y los cambios de estado que se producen en el teléfono. La aplicación no puede invocar ninguna operación en el dispositivo telefónico que cambiaría su estado, por lo que solo se pueden invocar las operaciones de estado. Varias aplicaciones pueden supervisar un dispositivo telefónico en un momento dado.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**propietario de PHONEPRIVILEGE \_**
</dt> <dd> <dl> <dt>



Una aplicación que abre un dispositivo telefónico con el privilegio Owner tiene permiso para cambiar el estado de las lámparas, el timbre, la pantalla, el conmutador y los bloques de datos del teléfono. La apertura de un dispositivo telefónico en modo propietario también proporciona la supervisión del dispositivo telefónico. Solo una aplicación puede ser el propietario de un dispositivo telefónico en un momento dado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




