---
description: Contiene información sobre un formulario de impresión localizable.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: FORM_INFO_2 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: fd933bf0ace6f394a801ab8dc4ef1fa30344b47966c09865a3aa4b713c6f2ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971524"
---
# <a name="form_info_2-structure"></a>Estructura de FORM \_ INFO \_ 2

Contiene información sobre un formulario de impresión localizable.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Propiedades del formulario. Se definen los siguientes valores, pero solo se puede establecer uno. Cuando [**GetForm**](getform.md) o [**EnumForms**](enumforms.md) **devuelven FORM \_ INFO \_ 2,** **flags** se establece en el valor actual de la base de datos de formularios.



| Value         | Significado                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| USUARIO DEL \_ FORMULARIO    | Si se establece esta marca de bits, el usuario ha definido el formulario. Los formularios con este conjunto de marcas se definen en el Registro.                                                                                                                                                                    |
| FORM \_ BUILTIN | Si se establece esta marca de bits, el formulario forma parte del colador. Las definiciones de formulario con este conjunto de marcas no aparecen en el Registro. Los formularios integrados no se pueden modificar, por lo que esta marca no debe establecerse cuando la estructura se pasa a [**AddForm**](addform.md) [**o SetForm.**](setform.md) |
| IMPRESORA DE \_ FORMULARIO | Si se establece esta marca de bits, el formulario se asocia a una impresora determinada y su definición aparece en el Registro.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del formulario. El nombre del formulario no puede superar los 31 caracteres.

</dd> <dt>

**Tamaño**
</dt> <dd>

Ancho y alto de la forma en milésimas de milímetros.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Ancho y alto, en milésimas de milímetros, del área de la página en la que se puede imprimir la impresora.

</dd> <dt>

**pKeyword**
</dt> <dd>

Puntero a un identificador de cadena no localizable del formulario. Cuando se pasa [**a AddForm**](addform.md) [**o SetForm,**](setform.md)esto proporciona al autor de la llamada un medio para identificar el formulario en todas las configuraciones regionales.

</dd> <dt>

**StringType**
</dt> <dd>

Especifica cómo se obtiene un nombre para mostrar localizado para el formulario en tiempo de ejecución. Se definen los valores siguientes. Solo se puede establecer una en una llamada determinada a [**AddForm**](addform.md) o [**SetForm.**](setform.md) String MUIDLL y STRING LANGPAIR se pueden establecer en el formulario \_ \_ INFO **\_ \_ 2** (s) devuelto por [**GetForm**](getform.md) o [**EnumForms**](enumforms.md). Vea la sección Comentarios.



| Value            | Significado                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRING \_ NONE     | No hay ningún nombre para mostrar localizado.                                                                                                                                                            |
| STRING \_ MUIDLL   | El nombre para mostrar se extrae del archivo [DLL Interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) recursos localizados especificado en **pMuiDll**. El identificador está en el **miembro dwResourceId.** |
| STRING \_ LANGPAIR | El nombre para mostrar y el identificador de idioma se proporcionan directamente mediante **pDisplayName** y **wLangId** especifica el idioma.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

El [Interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) dll de recursos localizados que contiene el nombre para mostrar localizado.

</dd> <dt>

**dwResourceId**
</dt> <dd>

Identificador de recurso del nombre para mostrar del formulario **en pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

Nombre para mostrar del formulario en el idioma especificado por **wLangId**.

</dd> <dt>

**wLangId**
</dt> <dd>

Idioma de **pDisplayName.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

En una llamada a [**AddForm**](addform.md) o [**SetForm**](setform.md):

-   Si **StringType** es STRING \_ NONE, **tanto pMuiDll** como **pDisplayName** deben ser **NULL** y **dwResourceId** y **wLangId** deben ser 0.
-   Si **StringType** es STRING \_ MUIDLL, **pDisplayName** debe ser **NULL** y **wLangId** debe ser 0.
-   Si **StringType** es STRING \_ LANGPAIR, **pMuiDll** debe ser **NULL** y **dwResourceId** debe ser 0.

Para un **FORMULARIO \_ INFO \_ 2** devuelto por una llamada a [**GetForm**](getform.md) o [**EnumForms**](enumforms.md):

-   Si **StringType** es STRING \_ MUIDLL y STRING \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** y **wLangId** tendrán valores válidos.
-   Si **StringType** solo es STRING \_ MUIDLL, **pMuiDll** y **dwResourceId** tendrán valores válidos. **pDisplayName** será **NULL y** **wLangId** será 0.
-   Si **StringType** solo es STRING \_ LANGPAIR, **pDisplayName** y **wLangId** tendrán valores válidos. **pMuiDll** será **NULL y** **dwResourceId** será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ FORM \_ INFO \_ 2W** (Unicode) y **\_ FORM INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

