---
description: El método SelectFile crea un comando de unidad de datos de protocolo de aplicación (APDU) que establece un archivo elemental actual dentro de un canal lógico. Los comandos subsiguientes pueden hacer referencia implícitamente al archivo actual a través del canal lógico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816:: SelectFile (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277017"
---
# <a name="iscardiso7816selectfile-method"></a>ISCardISO7816:: SelectFile (método)

\[El método **SelectFile** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **SelectFile** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que establece un archivo elemental actual dentro de un canal lógico. Los comandos subsiguientes pueden hacer referencia implícitamente al archivo actual a través del canal lógico.

La selección de un directorio (DF) en el almacén de almacén de la tarjeta (que puede ser la raíz (MF) del almacén de almacén) lo convierte en el DF actual. Después de esta selección, se puede hacer referencia a un archivo elemental actual implícito a través de ese canal lógico.

Al seleccionar un archivo elemental, se establece el archivo seleccionado y su elemento primario como archivos actuales.

Después de la respuesta al restablecimiento, el MF se selecciona implícitamente a través del canal lógico básico, a menos que se especifique de manera diferente en los bytes históricos o en la cadena de datos inicial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byP1* \[ de\]
</dt> <dd>

Control de selección.



| P1 (byte superior de Word): 8 7 6 5 4 3 2 1                                                                                                                                                            | Significado                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000xx**</dt><dt></dt> </dl> | Seleccionar ID. de archivo<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF, DF o MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | DF secundario<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | EF en DF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | DF primario del DF actual<br/> |



 

Cuando P1 = 00, la tarjeta sabe bien debido a una codificación específica del identificador de archivo o debido al contexto de ejecución del comando si el archivo que se va a seleccionar es MF, un DF o un EF.

Cuando P1-P2 = 0000, si se proporciona un identificador de archivo, será único en los entornos siguientes:

-   Elementos secundarios inmediatos del DF actual
-   DF primario
-   Elementos secundarios inmediatos del DF primario

Si P1-P2 = 0000 y el campo de datos está vacío o es igual a 3F00, seleccione el MF.

Cuando P1 = 04, el campo de datos es un nombre de DF, posiblemente truncado.

Cuando se admiten, los comandos sucesivos con el mismo campo de datos deben seleccionar DFs cuyos nombres coincidan con el campo de datos (es decir, empezar con el campo de datos de comando). Si la tarjeta acepta el comando con un campo de datos vacío, todos o un subconjunto del DFs se pueden seleccionar sucesivamente.

</dd> <dt>

*byP2* \[ de\]
</dt> <dd>

Control de selección.

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Datos de la operación si es necesario; en caso contrario, **null**. Entre los tipos de datos que se pasan en este parámetro se incluyen:

-   IDENTIFICADOR de archivo
-   Ruta de acceso del MF
-   Ruta de acceso del DF actual
-   Nombre de DF

</dd> <dt>

*lBytesToRead* \[ de\]
</dt> <dd>

Vacío (es decir, 0) o longitud máxima de los datos esperados en la respuesta.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

A menos que se especifique lo contrario, la ejecución correcta del comando encapsulado modifica el estado de seguridad de acuerdo con las siguientes reglas:

-   Cuando se cambia el archivo elemental actual, o cuando no hay ningún archivo elemental actual, se pierde el estado de seguridad específico de un archivo elemental actual anterior.
-   Cuando el directorio de almacén de información (DF) actual es descendiente de, o idéntico al DF anterior, se pierde el estado de seguridad específico del DF anterior actual. Se mantiene el estado de seguridad común a todos los antecesores comunes del DF anterior y el nuevo actual.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
