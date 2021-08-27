---
title: Método GetStringProperty de la Win32_RDMSVirtualDesktopCollection clase
description: Recupera una propiedad de cadena de una colección de escritorios virtuales.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto método , GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a0fae8a36110ffe2caccb9937ce67cf1b9d1515473eb6d7e0a2efec64dccfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033735"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método GetStringProperty de la clase \_ RDMSVirtualDesktopCollection de Win32

Recupera una propiedad de cadena de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que identifica la propiedad que se debe recuperar.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Cadena que recibe el valor recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDMSVirtualDesktopCollection de Win32 \_**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





