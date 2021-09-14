---
title: Método Network.setProxySettings
description: El método setProxySettings especifica la configuración de proxy para un protocolo determinado.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- Método setProxySettings Reproductor de Windows Media
- Método setProxySettings Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media método , setProxySettings
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243224"
---
# <a name="networksetproxysettings-method"></a>Método Network.setProxySettings

El **método setProxySettings** especifica la configuración de proxy para un protocolo determinado.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*protocolo* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> <dt>

*configuración* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene uno de los valores siguientes.



| Value | Descripción                                                          |
|-------|----------------------------------------------------------------------|
| 0     | No usar ningún servidor proxy.                                           |
| 1     | Use la configuración de proxy del explorador actual (solo válido para HTTP). |
| 2     | Use la configuración de proxy especificada manualmente.                           |
| 3     | Detecte automáticamente la configuración del proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se produce un error en este método a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se JScript con un elemento SELECT HTML para permitir al usuario especificar la configuración de proxy Reproductor de Windows Media para **el protocolo HTTP. El objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





