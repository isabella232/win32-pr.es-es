---
description: La clase WBEMTime facilita las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C. Para obtener más información, consulte también métodos de la clase WBEMTimeSpan.
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: Clase WBEMTime (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 5d2f06b06db998dc18a876e0e5534e1d86c6ae89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717118"
---
# <a name="wbemtime-class"></a>Clase WBEMTime

\[La clase **WBEMTime** forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

La clase **WBEMTime** facilita las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C. Para obtener más información, consulte también métodos de la [**clase WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Miembros

La clase **WBEMTime** tiene estos tipos de miembros:

-   [Constructores](#constructors)
-   [Métodos](#methods)

### <a name="constructors"></a>Constructores

La clase **WBEMTime** tiene estos constructores.



| Constructor                           | Descripción                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Constructor que facilita las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C.<br/> |



 

### <a name="methods"></a>Métodos

La clase **WBEMTime** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Claridad**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Establece la hora del objeto **WBEMTime** en una hora no válida.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Presenta la hora como un valor **BSTR** .<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Obtiene la hora como un valor **BSTR** en formato de fecha y hora de CIM.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Obtiene una fecha DMTF que se basa en un formato FAT o de [fecha y hora](date-and-time-format.md) en el que no se conoce la hora UTC.<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Obtiene la hora como una estructura **FILETIME** de MFC.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Sobrecargado. Devuelve el desplazamiento en minutos (+ o-) entre GMT y la hora local para el tiempo proporcionado en el argumento.<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Obtiene la hora como estructura **TM** en tiempo de ejecución de ANSI C.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Obtiene la hora como una estructura **SYSTEMTIME** de MFC.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Obtiene la hora como un entero de 64 bits.<br/>                                                                                          |
| [**GetTime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Obtiene la hora como una variable de tiempo de ejecución t de ANSI C \_ .<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indica si el objeto **WBEMTime** representa una hora válida.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Establece la hora en el objeto **WBEMTime** en formato de fecha y hora de CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Operadores sobrecargados de WBEMTime

El objeto **WBEMTime** define los siguientes operadores sobrecargados.



| Operadores sobrecargados de WBEMTime                                                                                                                                                                                                                                                                                                                                                                                                                                        | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operador =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | El operador de *asignación* facilita las conversiones entre varios formatos de tiempo de ejecución de Windows y ANSI C.                           |
| [**operador +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | El operador de *suma* incrementa la hora de un objeto en un intervalo de tiempo. El resultado se devuelve en un nuevo objeto **WBEMTime** .              |
| [**operador + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | El operador *Add-and-Assign* incrementa la hora de un objeto en un intervalo de tiempo.                                                             |
| [**Operator**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | El operador de *resta* reduce la hora de un objeto por la hora de otro objeto. El resultado se devuelve en un nuevo objeto **WBEMTime** . |
| [**operador-=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | El operador de *resta y asignación* reduce la hora de un objeto en un intervalo de tiempo.                                                        |
| [**Operator = =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)([**operador)! =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**operador >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**operador >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**operador <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**operador <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Los operadores de comparación comparan dos objetos **WBEMTime** .                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

