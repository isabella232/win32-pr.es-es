---
description: La estructura PROPERTYINST define una instancia de una propiedad en un fragmento de datos reconocidos. Monitor de red asigna y rellena una estructura PROPERTYINST cuando se adjunta una propiedad a la captura.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Estructura PROPERTYINST (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362135"
---
# <a name="propertyinst-structure"></a>PROPERTYINST (estructura)

La **estructura PROPERTYINST** define una instancia de una propiedad en un fragmento de datos reconocidos. Monitor de red asigna y rellena una estructura **PROPERTYINST** cuando se adjunta una propiedad a la captura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>Members

<dl> <dt>

**lpPropertyInfo**
</dt> <dd>

Puntero a la [estructura PROPERTYINFO](propertyinfo.md) que define la propiedad .

</dd> <dt>

**szPropertyText**
</dt> <dd>

Puntero a una cadena que se muestra en el panel de detalles de la interfaz Monitor de red usuario.

</dd> <dt>

**lpData**
</dt> <dd>

Puntero al inicio de los datos de la propiedad . El analizador determina dónde se inician los datos de propiedad.

</dd> <dt>

**lpByte**
</dt> <dd>

Puntero a los **datos BYTE.**

</dd> <dt>

**lpWord**
</dt> <dd>

Puntero a los **datos de WORD.**

</dd> <dt>

**lpDword**
</dt> <dd>

Puntero a los **datos DWORD.**

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Puntero a los [**datos LARGEINT.**](largeint.md)

</dd> <dt>

**lpSysTime**
</dt> <dd>

Puntero a los [**datos SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

Puntero a una [estructura PROPERTYINSTEX.](propertyinstex.md) El **miembro lpPropertyInstEx** solo se usa cuando se llama [a AttachPropertyInstanceEx.](attachpropertyinstanceex.md)

Si **se usa lpPropertyInstEx,** debe establecer el **miembro DataLength** en 0xFFFF.

</dd> <dt>

**DataLength**
</dt> <dd>

Longitud de datos para esta instancia de la propiedad . Si el **miembro lpPropertyInstEx** apunta a una estructura [**PROPERTYINSTEX,**](propertyinstex.md) debe establecer **DataLength** en 0xFFFF.

</dd> <dt>

**Level**
</dt> <dd>

Información de nivel.

</dd> <dt>

**HelpID**
</dt> <dd>

Identificador de contexto del archivo de ayuda.

</dd> <dt>

**IFlags**
</dt> <dd>

Marca de condición de error.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura PROPERTYINST** define una instancia de una propiedad adjunta. El analizador tiene acceso a la **estructura PROPERTYINST** a través de varias funciones auxiliares. Por ejemplo, cuando se llama a la función [**FormatPropertyInstance**](formatpropertyinstance.md) para dar formato a los datos de una propiedad, modifica el miembro **szPropertyText** de la **estructura PROPERTYINST.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

