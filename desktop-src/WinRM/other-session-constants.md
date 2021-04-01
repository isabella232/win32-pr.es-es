---
title: Otras constantes de sesión (WSManDisp. h)
description: Especifique la codificación, el cifrado y el puerto de nombre de entidad de seguridad de servicio.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150936"
---
# <a name="other-session-constants"></a>Otras constantes de sesión

Constantes, enumeradas en la lista siguiente, en la enumeración **\_ \_ WSManSessionFlags** que especifican la codificación, el cifrado y el puerto de nombre de entidad de seguridad de servicio.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Envía la solicitud en UTF8 en lugar de UTF16.

El método de scripting asociado es [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) y el método de C++ es [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



No Cifre los mensajes enviados a través de la red. Esta configuración solo se permite si el [*agente de escucha*](windows-remote-management-glossary.md) está configurado de modo que **AllowUnencrypted** esté establecido en **true**.

El método de scripting asociado es [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) y el método de C++ es [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Especifique el puerto de nombre de entidad de seguridad de servicio (SPN) al conectarse directamente al hardware de BMC remoto, también conocido como conexión [*fuera de banda*](windows-remote-management-glossary.md) . Dado que el equipo servidor WinRM y el hardware de BMC pueden compartir la misma dirección IP, esta marca indica que se debe usar el número de puerto de SPN para determinar si la conexión es al servicio o directamente al BMC. Para obtener más información, vea [formatos de nombre para SPN únicos](/windows/desktop/AD/name-formats-for-unique-spns).

El método de scripting asociado es [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) y el método de C++ es [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



Envía la solicitud en UTF16.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de sesión](session-constants.md)
</dt> </dl>

 

