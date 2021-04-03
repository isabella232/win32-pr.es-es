---
description: Devuelve una representación XML de un objeto o una instancia. Se da formato al archivo de texto en el formato XML especificado como se muestra en WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Método SWbemObjectEx.GetText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083337"
---
# <a name="swbemobjectexgettext_-method"></a>SWbemObjectEx. GetText ( \_ método)

El **método \_ gettext** del objeto [**SWBEMOBJECTEX**](swbemobjectex.md) devuelve una representación XML de un objeto o una instancia. Se da formato al archivo de texto en el formato XML especificado como se muestra en [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iTextFormat* \[ de\]
</dt> <dd>

Obligatorio. Un valor de [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) que especifica el formato XML resultante.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Marcas de operación reservadas. El valor predeterminado es 0 (cero).

</dd> <dt>

*objWbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que establece el contexto de la operación. El valor predeterminado es null. Para obtener más información sobre los pares de nombre/valor permitidos, vea la sección Comentarios a continuación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no tiene ningún valor devuelto.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ gettext** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

No se encontró el formato solicitado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Uno de los parámetros de la llamada no es correcto.

</dd> <dt>

**wbemErrCriticalError** -2147749898 (0x8004100A)
</dt> <dd>

Se produjo un error interno, grave e inesperado. Comunique este error al Servicio de soporte técnico de Microsoft.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al construir [**SWbemNamedValueSet**](swbemnamedvalueset.md), solo se permiten los siguientes pares de nombre/valor.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LocalOnly</td>
<td><strong>VT_BOOL</strong><br/> Si <strong>es true</strong>, solo las propiedades y los métodos definidos localmente están presentes en el XML resultante. El valor predeterminado es <strong>false</strong>.<br/></td>
</tr>
<tr class="even">
<td>IncludeQualifiers</td>
<td><strong>VT_BOOL</strong><br/> Si <strong>es true</strong>, los calificadores de clases, instancias, propiedades y métodos se incluyen en el XML resultante. El valor predeterminado es <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td>PathLevel</td>
<td><strong>VT-I4</strong><br/> El valor predeterminado es 0 (cero). Los valores posibles son:<br/>
<ul>
<li>0: <CLASS> <INSTANCE> se crea un elemento o en función de si el objeto es una clase o una instancia.</li>
<li>1: <VALUE.NAMEDOBJECT> se genera un elemento.</li>
<li>2: <VALUE.OBJECTWITHLOCALPATH> se genera un elemento.</li>
<li>3: <VALUE.OBJECTWITHPATH> se genera un elemento.</li>
</ul></td>
</tr>
<tr class="even">
<td>ExcludeSystemProperties</td>
<td><strong>VT-BOOL</strong><br/> Si <strong>es true</strong>, las propiedades del sistema, como __NAMESPACE, se excluyen de la salida.<br/></td>
</tr>
<tr class="odd">
<td>IncludeClassOrigin</td>
<td><strong>VT_BOOL</strong><br/> Si es <strong>true</strong>, se establece el atributo de origen de clase en los <PROPERTY> <METHOD> elementos y. El valor predeterminado es <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

Para obtener más información sobre cómo crear un [**SWbemNamedValueSet**](swbemnamedvalueset.md), vea [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).

## <a name="examples"></a>Ejemplos

El siguiente script muestra cómo obtener una representación XML de la definición de clase de [**\_ BIOS de Win32**](/windows/desktop/CIMWin32Prov/win32-bios) . Al especificar una instancia concreta del **\_ BIOS de Win32**, puede obtener los datos de ese objeto en XML.


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | \_ISWBEMOBJECTEX IID<br/>                                                          |



 

