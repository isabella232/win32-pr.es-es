---
title: TITLEBAR_TYPE enumeración (Softkbdc.h)
description: Los elementos de la enumeración TITLEBAR TYPE se usan para especificar tipos de barras de título que están disponibles \_ para una ventana de teclado flexible.
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
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068799"
---
# <a name="titlebar_type-enumeration"></a>Enumeración TITLEBAR \_ TYPE

Los elementos de la **enumeración TITLEBAR \_ TYPE** se usan para especificar tipos de barras de título que están disponibles para una ventana de teclado flexible.

## <a name="syntax"></a>Sintaxis


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

La ventana de teclado flexible solo usa una barra de control horizontal.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR \_ GRIPPER \_ VERTI \_ ONLY**
</dt> <dd>

La ventana de teclado flexible solo usa una barra de control vertical.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**BOTÓN DE \_ CONTROL DE LA BARRA DE \_ TÍTULO**
</dt> <dd>

La ventana de teclado flexible usa solo un botón de control.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |



 

 





