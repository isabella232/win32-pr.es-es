---
description: La clase WBEMTime facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución. Para obtener más información, vea también WBEMTimeSpan (Métodos de clase).
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
ms.openlocfilehash: 16b4e8933113386e877aec23313f74695b321f932c10f0e2730bcf5888675cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553251"
---
# <a name="wbemtime-class"></a>WBEMTime (clase)

\[La **clase WBEMTime** forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

La **clase WBEMTime** facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución. Para obtener más información, vea también [**Métodos de clase WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Miembros

La **clase WBEMTime** tiene estos tipos de miembros:

-   [Constructores](#constructors)
-   [Métodos](#methods)

### <a name="constructors"></a>Constructores

La **clase WBEMTime** tiene estos constructores.



| Constructor                           | Descripción                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Constructor que facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución.<br/> |



 

### <a name="methods"></a>Métodos

La **clase WBEMTime** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Borrar**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Establece la hora del objeto **WBEMTime** en una hora no válida.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Presenta la hora como un **valor BSTR.**<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Obtiene la hora como un **valor BSTR** en formato de fecha y hora CIM.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Obtiene una fecha DMTF que se basa en fat o en un [formato](date-and-time-format.md) de fecha y hora en el que no se conoce la hora UTC.<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Obtiene la hora como una estructura **FILETIME de** MFC.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Sobrecargado. Devuelve el desplazamiento en minutos (+ o -) entre GMT y la hora local para la hora proporcionada en el argumento .<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Obtiene la hora como estructura tm de estructura en tiempo de ejecución **de** ANSI C.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Obtiene la hora como una estructura **SYSTEMTIME de** MFC.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Obtiene la hora como un entero de 64 bits.<br/>                                                                                          |
| [**Gettime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Obtiene la hora como una variable t de tiempo de ejecución de ANSI \_ C.<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indica si el **objeto WBEMTime** representa una hora válida.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Establece la hora del objeto **WBEMTime** en formato de fecha y hora CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Operadores sobrecargados WBEMTime

El **objeto WBEMTime** define los siguientes operadores sobrecargados.



| Operadores sobrecargados WBEMTime                                                                                                                                                                                                                                                                                                                                                                                                                                        | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operator =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *El* operador de asignación facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución.                           |
| [**operador +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | *El* operador de suma incrementa el tiempo de un objeto en un intervalo de tiempo. El resultado se devuelve en un nuevo **objeto WBEMTime.**              |
| [**operador +=**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | *El operador Add-and-Assign* incrementa el tiempo de un objeto en un intervalo de tiempo.                                                             |
| [**operador :**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *El operador* de resta disminuye la hora de un objeto por la hora de otro objeto. El resultado se devuelve en un nuevo **objeto WBEMTime.** |
| [**operator -=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | *El operador Subtract-and-assign* disminuye el tiempo de un objeto en un intervalo de tiempo.                                                        |
| [**operator ==**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**operator !=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**operador >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**operator >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**operador <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**operator <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Los operadores de comparación comparan dos **objetos WBEMTime.**                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

