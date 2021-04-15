---
title: Constantes de EAPHost (Eaptypes. h)
description: Ver una lista de constantes de EAPHost (Eaptypes. h) que usan los métodos de EAPHost y ver los requisitos para su uso.
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
ms.openlocfilehash: 84704e59ed43466c47435f4804cb4dedc9c3a92d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421397"
---
# <a name="eaphost-constants"></a>Constantes de EAPHost

Constantes utilizadas por los métodos de EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**versión de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



La versión de los datos de interfaz de usuario interactiva de EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_versión de credenciales EAP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



La versión de las credenciales de EAP suministradas por el usuario.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**\_versión de \_ API del mismo nivel de EAPHOST \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



La versión de la API del mismo nivel de EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_longitud del hash del certificado \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Longitud del hash SHA1 del certificado.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**longitud máxima del \_ campo de entrada de configuración de EAP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Especifica la longitud máxima admitida de un campo de entrada.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**longitud máxima del \_ valor del campo de entrada de configuración de EAP \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Especifica la longitud máxima admitida de un campo de entrada.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**\_ \_ \_ \_ propiedades \_ predeterminadas del campo de entrada de la interfaz de usuario EAP**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista con SP1 o posterior: representa el valor de propiedad predeterminado para las entradas de campo de entrada que se muestran en la interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**propiedades de campo de entrada de configuración de EAP \_ \_ \_ \_ \_ predeterminada**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Representa el valor de propiedad predeterminado para las entradas de campo de entrada de configuración que se muestran en la interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**propiedades de los campos de entrada de la \_ interfaz de usuario EAP \_ \_ \_ \_ no \_ displayable**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista con SP1 o posterior: especifica que las entradas del campo de entrada no se mostrarán en la interfaz de usuario (por ejemplo, una contraseña o un número PIN).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**propiedades de campo de entrada de configuración de EAP \_ \_ \_ \_ \_ no \_ displayable**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Especifica que las entradas del campo de entrada de configuración no se mostrarán en la interfaz de usuario (por ejemplo, una contraseña o un número PIN).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**propiedades de campo de entrada de IU de EAP \_ \_ \_ \_ \_ no \_ persistentes**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista con SP1 o posterior: indica que el método EAP no almacenará en caché los datos de campo. El suplicante debe almacenar en caché los datos de campo para la itinerancia.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**propiedades de los campos de entrada de la \_ interfaz de usuario EAP \_ \_ \_ \_ \_ solo lectura**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista con SP1 o posterior: indica que el campo de entrada es de solo lectura y no se puede editar.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/> |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/> |



 

 





