---
title: Enumeración TITLEBAR_TYPE (Softkbdc. h)
description: Los elementos de la \_ enumeración de tipo TITLEBAR se usan para especificar los tipos de titlebars que están disponibles para una ventana de teclado en pantalla.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Marco de servicios de texto de enumeración de TITLEBAR_TYPE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685990"
---
# <a name="titlebar_type-enumeration"></a>\_Enumeración de tipo TITLEBAR

Los elementos de la enumeración de **\_ tipo TITLEBAR** se usan para especificar los tipos de titlebars que están disponibles para una ventana de teclado en pantalla.

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

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ None**
</dt> <dd>

La ventana teclado en pantalla no usa ninguna TitleBar.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**solo el agarrador de la TITLEBAR \_ \_ horiz \_**
</dt> <dd>

La ventana teclado en pantalla usa solo una barra de redimensionamiento horizontal.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**\_solo Vert (agarrador de TITLEBAR) \_ \_**
</dt> <dd>

La ventana teclado en pantalla solo usa una barra de redimensionamiento vertical.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**botón de sujeción de la TITLEBAR \_ \_**
</dt> <dd>

La ventana teclado en pantalla solo usa un botón de agarrador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





