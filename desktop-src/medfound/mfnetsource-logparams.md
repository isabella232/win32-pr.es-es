---
description: Matriz de cadenas con los parámetros que se van a enviar al servidor de registro.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Propiedad MFNETSOURCE_LOGPARAMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001498"
---
# <a name="mfnetsource_logparams-property"></a>\_Propiedad LOGPARAMS de MFNETSOURCE

Matriz de cadenas con los parámetros que se van a enviar al servidor de registro.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**WCHAR \** _

VT \_ LPWStr

_ *pwszVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ LOGPARAMS** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




