---
title: Constantes de EAPHost (Eaptypes.h)
description: Vea una lista de constantes de EAPHost (Eaptypes.h) que usan los métodos EAPHost y vea los requisitos para su uso.
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab336b147557722f1bec72bfe662b12599a64ee1622b31bdad6a92a05af6d92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119483015"
---
# <a name="eaphost-constants"></a>Constantes de EAPHost

Constantes utilizadas por los métodos EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**VERSIÓN DE \_ DATOS DE LA INTERFAZ DE USUARIO INTERACTIVA \_ \_ \_ DE EAP**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



La versión de los datos de la interfaz de usuario interactiva de EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**VERSIÓN DE CREDENCIALES DE EAP \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Versión de las credenciales de EAP proporcionadas por el usuario.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**VERSIÓN DE \_ LA API DEL MISMO NIVEL DE \_ \_ EAPHOST**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



La versión de la API del mismo nivel de EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**LONGITUD \_ DE HASH DE \_ CERTIFICADO**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Longitud del hash SHA1 del certificado.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**LONGITUD \_ MÁXIMA DEL CAMPO DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ \_ EAP**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Especifica la longitud máxima admitida de un campo de entrada.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**LONGITUD \_ MÁXIMA DEL VALOR DEL CAMPO DE ENTRADA DE CONFIGURACIÓN DE \_ \_ \_ \_ \_ EAP**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Especifica la longitud máxima admitida de un campo de entrada.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**VALOR PREDETERMINADO \_ DEL CAMPO DE ENTRADA DE LA INTERFAZ DE USUARIO \_ \_ \_ DE \_ EAP**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista con SP1 o posterior: representa el valor de propiedad predeterminado para las entradas de campo de entrada que se muestran en la interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**EAP \_ CONFIG \_ INPUT \_ FIELD \_ PROPS \_ DEFAULT**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Representa el valor de propiedad predeterminado para las entradas de campo de entrada de configuración que se muestran en la interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**PROPIEDADES DE CAMPO DE ENTRADA DE LA INTERFAZ DE USUARIO DE EAP \_ \_ NO SE PUEDEN \_ \_ \_ \_ MOSTRAR**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista con SP1 o posterior: especifica que las entradas de campo de entrada no se mostrarán en la interfaz de usuario (por ejemplo, una contraseña o un número de PIN).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**PROPIEDADES DE CAMPO DE ENTRADA DE CONFIGURACIÓN DE EAP \_ \_ NO SE PUEDEN \_ \_ \_ \_ MOSTRAR**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Especifica que las entradas del campo de entrada de configuración no se mostrarán en la interfaz de usuario (por ejemplo, una contraseña o un número de PIN).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**PROPIEDADES DE CAMPO DE ENTRADA DE LA INTERFAZ DE USUARIO DE EAP \_ \_ NO \_ \_ \_ \_ PERSISTENTES**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista con SP1 o posterior: indica que el método EAP no almacenará en caché los datos de campo; el suplicante debe almacenar en caché los datos de campo para la itinerancia.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**PROPIEDADES DE CAMPO DE ENTRADA DE LA INTERFAZ DE USUARIO DE EAP \_ \_ DE SOLO \_ \_ \_ \_ LECTURA**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista con SP1 o posterior: indica que el campo de entrada es de solo lectura y no se puede editar.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Role | Versión mínima del sistema operativo admitida |
|------|------------------------------|
| Cliente<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/> |
| Server<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



 

 





