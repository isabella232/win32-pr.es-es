---
title: Enumeración TYPEMODE (Softkbdc.h)
description: Los elementos de la enumeración TYPEMODE se usan para especificar modos de tipo que están disponibles para un teclado flexible.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Enumeración TYPEMODE Text Services Framework
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
ms.openlocfilehash: 4f9ae25435b48d1482441b8617a52bace8debabb210b62782a234837553e2c36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949842"
---
# <a name="typemode-enumeration"></a>Enumeración TYPEMODE

Los elementos de la **enumeración TYPEMODE** se usan para especificar modos de tipo que están disponibles para un teclado flexible.

## <a name="syntax"></a>Syntax


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

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Suspender**
</dt> <dd>

El usuario puede apuntar a una clave durante un período de tiempo predefinido y el carácter seleccionado se escribe automáticamente.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Escaneo**
</dt> <dd>

El teclado flexible examina continuamente el área de entrada y resalta las regiones en las que el usuario puede presionar una tecla de método abreviado o usar un dispositivo de entrada de conmutador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |



 

 





