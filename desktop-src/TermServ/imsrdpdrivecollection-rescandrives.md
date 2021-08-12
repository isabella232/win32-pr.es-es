---
title: Método IMsRdpDriveCollection RescanDrives
description: Actualiza la lista de objetos de la colección. | Método IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Método RescanDrives Servicios de Escritorio remoto
- Método RescanDrives Servicios de Escritorio remoto , interfaz IMsRdpDriveCollection
- Interfaz IMsRdpDriveCollection Servicios de Escritorio remoto , método RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2490e3879420701537cd36999ba33fde9ebfaf1e2f93d75550807e552fadacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606192"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>IMsRdpDriveCollection::RescanDrives (método)

Actualiza la lista de objetos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vboolDynRedir* \[ En\]
</dt> <dd>

El estado de redireccionamiento predeterminado que se aplicará a los dispositivos o unidades recién detectados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID IMsRdpDriveCollection se define como \_ 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





