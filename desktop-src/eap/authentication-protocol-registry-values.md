---
title: Valores de registro del Protocolo de autenticación
description: El software de instalación de la DLL EAP puede crear los siguientes valores del registro bajo eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104077162"
---
# <a name="authentication-protocol-registry-values"></a>Valores de registro del Protocolo de autenticación

El software de instalación de la DLL EAP puede crear los siguientes valores del registro bajo **&lt; eaptypeid &gt;**. Estos valores del registro se definen en el archivo de encabezado Raseapif. h. Los valores **RAS_EAP_VALUENAME_PATH** y **RAS_EAP_VALUENAME_FRIENDLY_NAME** son obligatorios. El software de instalación también puede crear otras claves y valores. Estos podrían ser usados por el propio protocolo de autenticación. Para obtener más información y un ejemplo de la configuración del registro, consulte [ejemplo de valores del registro](registry-values-example.md).

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Configur

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| Valor constante | Path                               |
|----------------|------------------------------------|
| Tipo           |  REG_EXPAND_SZ                     |
| Descripción    | Especifica la ruta de acceso al archivo DLL de EAP. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Valor constante | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_SZ                                                                                                                                                           |
| Descripción    | Especifica un nombre descriptivo para el protocolo de autenticación. Este nombre aparece en la interfaz de usuario de la aplicación EAP para implementaciones de acceso telefónico e inalámbricas. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Valor constante | ConfigUIPath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Tipo           |  REG_EXPAND_SZ                                                                                                                    |
| Descripción    | Especifica la ruta de acceso al archivo DLL que implementa la interfaz de usuario de configuración en el cliente, ya que esta interfaz de usuario es solo para el cliente. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Valor constante | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| Tipo           | REG_BINARY                                                           |
| Descripción    | Especifica los datos de configuración predeterminados para el protocolo de autenticación. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Valor constante | RequireConfigUI                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                                                                               |
| Descripción    | Especifica si el usuario debe proporcionar datos de configuración en la interfaz de usuario de la aplicación cliente EAP. Si este valor es 1, no se permite que el usuario salga de la interfaz de usuario de la aplicación cliente EAP sin proporcionar datos de configuración. El valor predeterminado es 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Valor constante | ConfigCLSID                                                   |
|----------------|---------------------------------------------------------------|
| Tipo           | REG_SZ                                                       |
| Descripción    | Especifica el ID. de clase de la interfaz de usuario de configuración en el servidor. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Valor constante | IdentityPath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           |  REG_EXPAND_SZ                                                                                                                         |
| Descripción    | Especifica la ruta de acceso al archivo DLL que implementa funciones para obtener la identidad del usuario en el cliente, ya que esta interfaz de usuario es solo para el cliente. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Valor constante | InteractiveUIPath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| Tipo           |  REG_EXPAND_SZ                                                                                                                  |
| Descripción    | Especifica la ruta de acceso al archivo DLL que implementa la interfaz de usuario interactiva en el cliente, ya que esta interfaz de usuario es solo para el cliente. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Valor constante | InvokeUsernameDialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                             |
| Descripción    | Especifica si RAS debe mostrar el cuadro de diálogo de nombre de usuario estándar de Windows NT/Windows 2000 (valor 1) o invocar [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valor 0). El valor predeterminado es 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Valor constante | InvokePasswordDialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                  |
| Descripción    | Especifica si RAS debe mostrar el cuadro de diálogo de contraseña estándar de Windows NT/Windows 2000. Si este valor existe y es 0, RAS no mostrará el cuadro de diálogo de contraseña. El valor predeterminado es 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Valor constante | MPPEEncryptionSupported                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                    |
| Descripción    | Si este valor es 1, el protocolo de autenticación puede generar claves para el estilo de cifrado punto a punto de Microsoft (MPPE) del cifrado. Los valores posibles son 0 o 1. El valor predeterminado es 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Valor constante | StandaloneSupported                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                     |
| Descripción    | Especifica si este protocolo de autenticación se admite en un servidor de Windows 2000 independiente. Un valor de 0 indica que no se admite EAP. El valor predeterminado es 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Valor constante | RolesSupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo           | REG_DWORD                                                                                                                                                                                                                                 |
| Descripción    | Especifica los distintos roles que admite el EAP. Indica si se puede usar en un servidor o en un cliente, si es compatible con conexiones RAS (VPN) o PEAP. El comportamiento predeterminado es mostrar el método EAP en PEAP y en EAP. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Valor constante | PerPolicyConfig |
|----------------|-----------------|
| Tipo           | REG_DWORD      |
| Descripción    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Este valor del registro no está en uso.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Este valor del registro no está en uso.

