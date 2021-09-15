---
title: ACCELTABLEENTRY (estructura)
description: Describe los datos de un recurso de tabla de aceleradores individual. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menús de estructura ACCELTABLEENTRY y otros recursos
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468575"
---
# <a name="acceltableentry-structure"></a>ACCELTABLEENTRY (estructura)

Describe los datos de un recurso de tabla de aceleradores individual. La definición de estructura que se proporciona aquí es solo para explicación; no está presente en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**fFlags**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Describe las características del acelerador de teclado. Este miembro puede tener uno o varios de los siguientes valores de Winuser.h.



| Value                                                                                                                                                                                                      | Significado                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>TRUE</dt> </dl>    | La tecla de aceleración es un [código de clave virtual.](/windows/desktop/inputdev/virtual-key-codes) Si no se especifica esta marca, se supone que la tecla de aceleración especifica un código de caracteres ASCII. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT**</dt> <dt>0x02</dt> </dl> | Un elemento de menú de la barra de menús no se resalta cuando se usa un acelerador. Este atributo está obsoleto y solo se conserva por compatibilidad con versiones anteriores con archivos de recursos diseñados para archivos de 16 Windows.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT**</dt> <dt>0x04</dt> </dl>          | El acelerador solo se activa si el usuario presiona la tecla MAYÚS. Esta marca solo se aplica a las claves virtuales. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL**</dt> <dt>0x08</dt> </dl>    | El acelerador solo se activa si el usuario presiona la tecla CTRL. Esta marca solo se aplica a las claves virtuales. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**FALT**</dt> <dt>0x10</dt> </dl>                | El acelerador solo se activa si el usuario presiona la tecla ALT. Esta marca solo se aplica a las claves virtuales. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | La entrada es la última de una tabla de aceleradores. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Valor de carácter ANSI o código de clave virtual que identifica la tecla de aceleración.

</dd> <dt>

**Wid**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificador del acelerador de teclado. Este es el valor que se pasa al procedimiento de ventana cuando el usuario presiona la tecla especificada.

</dd> <dt>

**padding**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de bytes insertados para asegurarse de que la estructura está alineada en un **límite DWORD.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura ACCELTABLEENTRY se** repite para todas las entradas de la tabla de aceleradores del recurso. La última entrada de la tabla se marca con el valor 0x0080.

Puede calcular el número de elementos de la tabla si divide la longitud del recurso entre ocho. A continuación, la aplicación puede acceder aleatoriamente a las entradas individuales de longitud fija.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

