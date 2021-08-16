---
description: Las constantes de marca de bits PHONEPRIVILEGE describen las distintas formas en que se puede abrir \_ un dispositivo de teléfono.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: PHONEPRIVILEGE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9b3f3848af8c9858522bd924ccb77d7bf1682f09b66c0cfdcb5527b93416dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761297"
---
# <a name="phoneprivilege_-constants"></a>Constantes PHONEPRIVILEGE \_

Las constantes de marca de bits **PHONEPRIVILEGE \_** describen las distintas formas en que se puede abrir un dispositivo de teléfono.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE \_ MONITOR**
</dt> <dd> <dl> <dt>



Se informa a una aplicación que abre un dispositivo telefónico con el privilegio de monitor sobre los eventos y los cambios de estado que se producen en el teléfono. La aplicación no puede invocar ninguna operación en el dispositivo telefónico que cambiaría su estado, por lo que solo se pueden invocar las operaciones de estado. Varias aplicaciones pueden supervisar un dispositivo de teléfono en un momento dado.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PROPIETARIO DE \_ PHONEPRIVILEGE**
</dt> <dd> <dl> <dt>



Una aplicación que abre un dispositivo telefónico con el privilegio de propietario puede cambiar el estado de las bombillas, el timbre, la pantalla, el conmutador de enlace y los bloques de datos del teléfono. La apertura de un dispositivo de teléfono en modo de propietario también proporciona supervisión del dispositivo telefónico. Solo se permite que una aplicación sea el propietario de un dispositivo de teléfono en un momento dado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




