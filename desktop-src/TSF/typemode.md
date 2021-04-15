---
title: Enumeración TYPEMODE (Softkbdc. h)
description: Los elementos de la enumeración TYPEMODE se usan para especificar los modos de tipo que están disponibles para un teclado en pantalla.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- TYPEMODE Enumeration Text Services Framework
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676653"
---
# <a name="typemode-enumeration"></a>Enumeración TYPEMODE

Los elementos de la enumeración **TYPEMODE** se usan para especificar los modos de tipo que están disponibles para un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**
</dt> <dd>

El usuario puede hacer clic en las teclas en pantalla para escribir texto.

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Activada**
</dt> <dd>

El usuario puede apuntar a una clave durante un período de tiempo predefinido, y el carácter seleccionado se escribe automáticamente.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Explora**
</dt> <dd>

El teclado en pantalla examina continuamente el área de entrada y resalta las regiones en las que el usuario puede presionar una tecla de método abreviado o usar un dispositivo de entrada de conmutador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





