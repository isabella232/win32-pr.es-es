---
title: IMsRdpClientAdvancedSettings CachePersistenceActive, propiedad
description: Especifica si se debe usar el almacenamiento en caché de mapa de bits persistente. El almacenamiento en caché persistente puede mejorar el rendimiento, pero requiere más espacio en disco.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Propiedad CachePersistenceActive Servicios de Escritorio remoto
- Propiedad CachePersistenceActive Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad CachePersistenceActive
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e9975bcfeca8ff5dfbedf3507003432cb4bd3167c794ecd0b690492caf3e40d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871185"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a>IMsRdpClientAdvancedSettings::CachePersistenceActive, propiedad

Especifica si se debe usar el almacenamiento en caché de mapa de bits persistente. El almacenamiento en caché persistente puede mejorar el rendimiento, pero requiere más espacio en disco.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





