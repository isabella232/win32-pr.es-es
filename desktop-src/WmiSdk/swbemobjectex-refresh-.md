---
description: Actualiza los datos de los objetos que tienen datos proporcionados por un proveedor de rendimiento, como las clases de contador de rendimiento. Puede obtener datos actualizados más rápidamente y sin una llamada a SWbemServices. Get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Método SWbemObjectEx.Refresh_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715734"
---
# <a name="swbemobjectexrefresh_-method"></a>SWbemObjectEx. Refresh ( \_ método)

El **método \_ Refresh** de [**SWbemObjectEx**](swbemobjectex.md) actualiza los datos de los objetos que tienen datos proporcionados por un proveedor de rendimiento, como las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes). Puede obtener datos actualizados más rápidamente y sin una llamada a [**SWbemServices. Get \_**](swbemservices-get.md).

Para obtener más información sobre esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Marcas de operación reservadas que, si se especifican, deben ser 0 (cero).

</dd> <dt>

*objWbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que establece el contexto de la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ Refresh** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Se produjo un error interno en el proveedor, aunque la operación era válida.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

No se encontró el formato solicitado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Uno de los parámetros de la llamada no es correcto.

</dd> <dt>

**wbemErrRefresherBusy** -2147749975 (0x80041057)
</dt> <dd>

El actualizador está ocupado con otra operación.

</dd> <dt>

**wbemPartialResults** -2147745808 (0x80040010)
</dt> <dd>

No todos los objetos, enumeradores o actualizaciones anidadas se actualizaron correctamente. Este valor devuelto no es un error, pero indica que la operación estaba incompleta.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo de código de script siguiente se muestra cómo obtener contadores de rendimiento sin procesar y cocidos para el proceso del sistema. Los objetos se actualizan cada dos segundos y se muestran las propiedades.


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Supervisión de datos de rendimiento](monitoring-performance-data.md)
</dt> </dl>

 

