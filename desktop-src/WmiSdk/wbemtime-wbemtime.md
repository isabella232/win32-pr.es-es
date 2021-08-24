---
description: El constructor de clase WBEMTime facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: Constructores WBEMTime::WBEMTime (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757625"
---
# <a name="wbemtimewbemtime-constructors"></a>Constructores WBEMTime::WBEMTime

\[La [**clase WBEMTime**](wbemtime.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

El constructor **de la clase WBEMTime** facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución.

### <a name="overload-list"></a>Lista de sobrecarga



| Constructor                                                                 | Descripción                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Crea un objeto de hora sin inicializar.<br/>                          |
| [**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Inicializa el nuevo objeto de hora en el valor del parámetro .<br/> |
| [**WBEMTime(const time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Inicializa el nuevo objeto de hora en el valor del parámetro .<br/> |
| [**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Inicializa el nuevo objeto de hora en el valor del parámetro .<br/> |
| [**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Inicializa el nuevo objeto de hora en el valor del parámetro .<br/> |
| [**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Inicializa el nuevo objeto de hora en el valor del parámetro .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
