---
title: TITLEBAR_TYPE enumeración (Softkbdc.h)
description: Los elementos de la enumeración TITLEBAR TYPE se usan para especificar tipos de barras de título \_ que están disponibles para una ventana de teclado flexible.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE enumeración Text Services Framework
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941892a7ddbbcac85d66a00a24c1e80f301ab13c8c46f734cae11d074bdff637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950402"
---
# <a name="titlebar_type-enumeration"></a>ENUMERACIÓN TITLEBAR \_ TYPE

Los elementos de la **enumeración TITLEBAR \_ TYPE** se usan para especificar tipos de barras de título que están disponibles para una ventana de teclado flexible.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ NONE**
</dt> <dd>

La ventana de teclado flexible no usa ninguna barra de título.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR \_ GRIPPER \_ HORIZ \_ ONLY**
</dt> <dd>

La ventana de teclado suave solo usa una barra de control horizontal.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR \_ GRIPPER \_ VERTI \_ ONLY**
</dt> <dd>

La ventana de teclado suave solo usa una barra de control vertical.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**BOTÓN DE \_ CONTROL DE LA BARRA DE \_ TÍTULO**
</dt> <dd>

La ventana de teclado suave solo usa un botón de control.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |



 

 





