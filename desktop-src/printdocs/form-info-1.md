---
description: La FORM_INFO_1 estructura contiene información sobre un formulario de impresión. La información incluye el origen de los formularios de impresión, su nombre, sus dimensiones y las dimensiones de su área imprimible.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: FORM_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6f620d8bd2ed4ef39fc868c91068e10a7ff43f57d98510ecfbae1dbe2ae7c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949265"
---
# <a name="form_info_1-structure"></a>FORM_INFO_1 estructura

La **FORM_INFO_1** estructura contiene información sobre un formulario de impresión. La información incluye el origen del formulario de impresión, su nombre, sus dimensiones y las dimensiones de su área imprimible.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Propiedades del formulario. Se definen los valores siguientes.



| Value         | Significado                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| Form_user    | Si se establece esta marca de bits, el usuario ha definido el formulario. Los formularios con este conjunto de marcas se definen en el Registro.        |
| FORM_BUILTIN | Si se establece esta marca de bits, el formulario forma parte del colador. Las definiciones de formulario con este conjunto de marcas no aparecen en el Registro. |
| FORM_PRINTER | Si se establece esta marca de bits, el formulario se asocia a una impresora determinada y su definición aparece en el Registro.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del formulario. El nombre del formulario no puede superar los 31 caracteres.

</dd> <dt>

**Tamaño**
</dt> <dd>

Ancho y alto, en milésimas de milímetros, del formulario.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Ancho y alto, en milésimas de milímetros, del formulario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **_FORM_INFO_1W** (Unicode) y **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




