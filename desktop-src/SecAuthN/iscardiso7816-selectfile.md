---
description: El método SelectFile construye un comando de unidad de datos de protocolo de aplicación (APDU) que establece un archivo elemental actual dentro de un canal lógico. Los comandos posteriores pueden hacer referencia implícitamente al archivo actual a través del canal lógico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: Método ISCardISO7816::SelectFile (Scardssp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244280"
---
# <a name="iscardiso7816selectfile-method"></a>Método ISCardISO7816::SelectFile

\[El **método SelectFile** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método SelectFile** construye un comando [*de*](../secgloss/a-gly.md) unidad de datos de protocolo de aplicación (APDU) que establece un archivo elemental actual dentro de un canal lógico. Los comandos posteriores pueden hacer referencia implícitamente al archivo actual a través del canal lógico.

Al seleccionar un directorio (DF) en el almacén de archivos de tarjeta , que puede ser la raíz (MF) del almacén de archivos, se convierte en el DF actual. Después de esta selección, se puede hacer referencia a un archivo elemental actual implícito a través de ese canal lógico.

Al seleccionar un archivo elemental, se establece el archivo seleccionado y su elemento primario como archivos actuales.

Después de la respuesta que se va a restablecer, la mf se selecciona implícitamente a través del canal lógico básico, a menos que se especifique de forma diferente en los bytes históricos o en la cadena de datos inicial.

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

*byP1* \[ En\]
</dt> <dd>

Control de selección.



| P1 (byte superior en palabra): 8 7 6 5 4 3 2 1                                                                                                                                                            | Significado                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000xx**</dt><dt></dt> </dl> | Seleccione Id. de archivo.<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF, DF o MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | DF secundario<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | EF en DF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | DF primario del DF actual<br/> |



 

Cuando P1=00, la tarjeta lo sabe debido a una codificación específica del identificador de archivo o al contexto de ejecución del comando si el archivo que se va a seleccionar es MF, DF o EF.

Cuando P1-P2=0000, si se proporciona un identificador de archivo, será único en los siguientes entornos:

-   Secundarios inmediatos del DF actual
-   DF primario
-   Elementos secundarios inmediatos del DF primario

Si P1-P2=0000 y el campo de datos está vacío o igual a 3F00, seleccione la MF.

Cuando P1=04, el campo de datos es un nombre DF, posiblemente truncado a la derecha.

Cuando se admite, los comandos sucesivos con el mismo campo de datos deben seleccionar archivos DF cuyos nombres coincidan con el campo de datos (es decir, comiencen por el campo de datos de comando). Si la tarjeta acepta el comando con un campo de datos vacío, se pueden seleccionar sucesivamente todos los archivos DF o un subconjunto de ellos.

</dd> <dt>

*byP2* \[ En\]
</dt> <dd>

Control de selección.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Datos para la operación si es necesario; else, **NULL**. Los tipos de datos que se pasan en este parámetro incluyen:

-   id. de archivo
-   ruta de acceso de MF
-   ruta de acceso del DF actual
-   Nombre df

</dd> <dt>

*lBytesToRead* \[ En\]
</dt> <dd>

Vacío (es decir, 0) o longitud máxima de los datos esperados en respuesta.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un [**objeto de interfaz ISCardCmd**](iscardcmd.md) o **NULL.**

Al devolverse, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve a través del *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

A menos que se especifique lo contrario, la ejecución correcta del comando encapsulado modifica el estado de seguridad según las reglas siguientes:

-   Cuando se cambia el archivo elemental actual o no hay ningún archivo elemental actual, se pierde el estado de seguridad específico de un archivo elemental actual anterior.
-   Cuando el directorio de almacén de archivos (DF) actual es descendiente de o idéntico al df actual anterior, se pierde el estado de seguridad específico del df actual anterior. Se mantiene el estado de seguridad común a todos los antecesores comunes del DF actual anterior y nuevo.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
