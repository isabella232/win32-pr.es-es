---
title: Método GetInt32Property de la Win32_RDMSVirtualDesktopCollection (Microsoft.diagnostics.appanalysis.h)
description: Recupera una propiedad de entero de una colección de escritorios virtuales.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection clase
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto , método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968495"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método GetInt32Property de la clase \_ RDMSVirtualDesktopCollection de Win32

Recupera una propiedad de entero de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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

Entero que recibe el valor recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                                 |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                                   |
| Encabezado<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RDMSVirtualDesktopCollection de Win32 \_**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





