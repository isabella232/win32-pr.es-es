---
title: Enumeración COLORTYPE (Softkbdc. h)
description: Los elementos de la enumeración COLORTYPE se usan para especificar los tipos de colores que están disponibles para un teclado en pantalla.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Plataforma de servicios de texto de enumeración COLORTYPE
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666043"
---
# <a name="colortype-enumeration"></a>Enumeración COLORTYPE

Los elementos de la enumeración **COLORTYPE** se usan para especificar los tipos de colores que están disponibles para un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**
</dt> <dd>

Color de fondo.

</dd> <dt>

<span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**
</dt> <dd>

Color de primer plano no seleccionado.

</dd> <dt>

<span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**
</dt> <dd>

Color de texto no seleccionado.

</dd> <dt>

<span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**
</dt> <dd>

Color de primer plano seleccionado.

</dd> <dt>

<span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**
</dt> <dd>

Color del texto seleccionado.

</dd> <dt>

<span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Tipo de color Max \_**
</dt> <dd>

Tipo de color máximo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





