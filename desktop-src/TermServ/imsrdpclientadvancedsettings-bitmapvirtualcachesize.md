---
title: IMsRdpClientAdvancedSettings BitmapVirtualCacheSize, propiedad
description: Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se usará para el color de 8 bits por píxel.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad BitmapVirtualCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ec0d02e71849af88212db733ee205cb26f8c72a5c67c00acaef528bf086423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353179"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a>IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize, propiedad

Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se usará para el color de 8 bits por píxel.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a>Valor de propiedad

Nuevo tamaño de caché. Los valores válidos son de 1 a 32 inclusive. Tenga en cuenta que el tamaño máximo de todos los archivos de caché virtual es de 128 MB.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Consulte también

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

[**BitmapVirtualCache16BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[**BitmapVirtualCache24BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





