---
title: IMsRdpDriveCollection RescanDrives, método
description: Actualiza la lista de objetos de la colección. | IMsRdpDriveCollection RescanDrives, método
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Método RescanDrives Servicios de Escritorio remoto
- Método RescanDrives Servicios de Escritorio remoto, interfaz IMsRdpDriveCollection
- Interfaz IMsRdpDriveCollection Servicios de Escritorio remoto, método RescanDrives
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
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689724"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a>IMsRdpDriveCollection:: RescanDrives (método)

Actualiza la lista de objetos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vboolDynRedir* \[ de\]
</dt> <dd>

El estado de redirección predeterminada que se aplicará a los dispositivos o unidades recién detectados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection se define como 7ff17599-da2c-4677-Ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





