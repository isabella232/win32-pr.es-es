---
description: Matriz de cadenas con los parámetros que se enviarán al servidor de registro.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba557c4fb0bf77693669e8cb46af269ec3a4f2ed72c536e4bdab53a0778dc038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113525"
---
# <a name="mfnetsource_logparams-property"></a>MFNETSOURCE \_ LOGPARAMS, propiedad

Matriz de cadenas con los parámetros que se enviarán al servidor de registro.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**Wchar\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Comentarios

La **constante MFNETSOURCE \_ LOGPARAMS** define el GUID de la clave de propiedad. El identificador de propiedad (PID) es cero. Para establecer esta propiedad en el origen de red, pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




