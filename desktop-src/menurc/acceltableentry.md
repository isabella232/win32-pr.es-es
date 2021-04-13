---
title: Estructura ACCELTABLEENTRY
description: Describe los datos de un recurso de tabla de aceleradores individual. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menús de la estructura ACCELTABLEENTRY y otros recursos
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492976"
---
# <a name="acceltableentry-structure"></a>Estructura ACCELTABLEENTRY

Describe los datos de un recurso de tabla de aceleradores individual. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**fFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Describe las características del acelerador del teclado. Este miembro puede tener uno o varios de los valores siguientes de Winuser. h.



| Value                                                                                                                                                                                                      | Significado                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>true</dt> </dl>    | La tecla de aceleración es un [código de tecla virtual](/windows/desktop/inputdev/virtual-key-codes). Si no se especifica esta marca, se supone que la tecla de aceleración especifica un código de carácter ASCII. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT**</dt> <dt>0x02</dt> </dl> | Los elementos de menú de la barra de menús no se resaltan cuando se utiliza un acelerador. Este atributo está obsoleto y solo se conserva por compatibilidad con versiones anteriores de los archivos de recursos diseñados para Windows de 16 bits.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT**</dt> <dt>0x04</dt> </dl>          | El acelerador solo se activa si el usuario presiona la tecla Mayús. Esta marca solo se aplica a las claves virtuales. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL**</dt> <dt>0x08</dt> </dl>    | El acelerador solo se activa si el usuario presiona la tecla CTRL. Esta marca solo se aplica a las claves virtuales. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**FALT**</dt> <dt>0x10</dt> </dl>                | El acelerador solo se activa si el usuario presiona la tecla ALT. Esta marca solo se aplica a las claves virtuales. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | La entrada es la última de una tabla de aceleradores. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Un valor de carácter ANSI o un código de tecla virtual que identifica la tecla de aceleración.

</dd> <dt>

**wId**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificador de la tecla de aceleración. Este es el valor que se pasa al procedimiento de ventana cuando el usuario presiona la tecla especificada.

</dd> <dt>

**padding**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Número de bytes insertados para asegurarse de que la estructura está alineada en un límite **DWORD** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **ACCELTABLEENTRY** se repite para todas las entradas de la tabla de aceleradores en el recurso. La última entrada de la tabla se marca con el valor 0x0080.

Puede calcular el número de elementos de la tabla si divide la longitud del recurso por ocho. A continuación, la aplicación puede tener acceso de forma aleatoria a las entradas individuales de longitud fija.

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

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> </dl>

 

