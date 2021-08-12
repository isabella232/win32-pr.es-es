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
ms.openlocfilehash: 6501d097a4ec342c2831e4b72bf8f17edc4e4e1bec02b2b51cd7840325674b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573863"
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



| Valor | Descripción                                                          |
|-------|----------------------------------------------------------------------|
| 0     | No usar ningún servidor proxy.                                           |
| 1     | Use la configuración de proxy del explorador actual (solo válido para HTTP). |
| 2     | Use la configuración de proxy especificada manualmente.                           |
| 3     | Detecte automáticamente la configuración del proxy.                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





