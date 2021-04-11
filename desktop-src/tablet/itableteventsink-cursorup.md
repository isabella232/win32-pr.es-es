---
description: Se produce cuando el usuario ha generado el lápiz óptico desde la superficie del digitalizador de Tablet PC.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'ITabletEventSink:: CursorUp (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279174"
---
# <a name="itableteventsinkcursorup-method"></a>ITabletEventSink:: CursorUp (método)

Se produce cuando el usuario ha generado el lápiz óptico desde la superficie del digitalizador de Tablet PC.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TCID* \[ de\]
</dt> <dd>

El identificador de la tableta.

</dd> <dt>

*CID* \[ en\]
</dt> <dd>

Identificador del lápiz óptico.

</dd> <dt>

*nSerialNumber* \[ de\]
</dt> <dd>

Número de serie del lápiz óptico.

</dd> <dt>

*cbPkt* \[ de\]
</dt> <dd>

El número de bytes de un paquete de datos del lápiz óptico.

</dd> <dt>

*pbPkt* \[ de\]
</dt> <dd>

Los datos del lápiz óptico que indican la ubicación en la que se ha levantado el lápiz óptico de la tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




