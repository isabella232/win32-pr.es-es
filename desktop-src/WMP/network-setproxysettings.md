---
title: Network. setProxySettings (método)
description: El método setProxySettings especifica la configuración de proxy para un protocolo determinado.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- método setProxySettings de Windows Media Player
- método setProxySettings Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699321"
---
# <a name="networksetproxysettings-method"></a>Network. setProxySettings (método)

El método **setProxySettings** especifica la configuración de proxy para un protocolo determinado.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Protocolo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).

</dd> <dt>

*configuración* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene uno de los valores siguientes.



| Value | Descripción                                                          |
|-------|----------------------------------------------------------------------|
| 0     | No usar ningún servidor proxy.                                           |
| 1     | Use la configuración de proxy del explorador actual (solo es válida para HTTP). |
| 2     | Utilice la configuración de proxy especificada manualmente.                           |
| 3     | Detectar automáticamente la configuración de proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa JScript con un elemento SELECT de HTML **para permitir al usuario especificar la configuración del proxy de Windows Media Player para el protocolo http. El objeto Player** se creó con ID = "Player".


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





