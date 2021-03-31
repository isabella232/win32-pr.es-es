---
description: El método GetLocalOffsetForDate devuelve el desplazamiento en minutos (+ o &\# 8211;) entre GMT y hora local para el tiempo proporcionado en el argumento.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Métodos WBEMTime:: GetLocalOffsetForDate (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911478"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>WBEMTime:: GetLocalOffsetForDate (métodos)

\[La clase [**WBEMTime**](wbemtime.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El método **GetLocalOffsetForDate** devuelve el desplazamiento en minutos (+ o) entre GMT y la hora local para el tiempo proporcionado en el argumento.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                           | Descripción                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**GetLocalOffsetForDate (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | El argumento es una referencia a un **tiempo \_ t**.<br/>  |
| [**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | El argumento es un puntero a un **FILETIME**.<br/>   |
| [**GetLocalOffsetForDate (struct TM \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | El argumento es un puntero a la estructura **TM** .<br/> |
| [**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | El argumento es un puntero a un **SYSTEMTIME**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
