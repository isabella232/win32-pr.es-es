---
description: Los operadores de asignación de clase WBEMTime se sobrecargan para facilitar las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C. A continuación se enumeran las diversas firmas sobrecargadas.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'WBEMTime:: Operator = Operators (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361521"
---
# <a name="wbemtimeoperator-operators"></a>Operadores WBEMTime:: Operator =

\[La clase [**WBEMTime**](wbemtime.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Los operadores de asignación de clase [**WBEMTime**](wbemtime.md) se sobrecargan para facilitar las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C. A continuación se enumeran las diversas firmas sobrecargadas.

### <a name="overload-list"></a>Lista de sobrecarga



| Operator                                                                     | Descripción                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**Operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Convierte un **BSTR** en el formato **WBEMTime** .<br/>         |
| [**Operator = (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Convierte la **hora \_ t** al formato **WBEMTime** .<br/>        |
| [**operador = (& FILETIME)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Convierte **FILETIME** en formato **WBEMTime** .<br/>       |
| [**Operator = (struct TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Convierte una estructura **TM** en el formato **WBEMTime** .<br/> |
| [**operador = (& SYSTEMTIME)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Convierte **SYSTEMTIME** en formato **WBEMTime** .<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
