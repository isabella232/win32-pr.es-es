---
title: Constantes de identidad (AppModel. h)
description: Especifica la longitud de las cadenas para los campos de identidad del paquete.
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681a0aef767afe92cdb93eee3849df8ed6a5f080
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705126"
---
# <a name="identity-constants"></a>Constantes de identidad

Especifica la longitud de las cadenas para los campos de identidad del paquete. La longitud se mide en caracteres y puede o no incluir espacio para el terminador NULL.

> [!Note]  
> Constantes de la forma: la longitud del identificador de modelo de usuario de la **aplicación \_ \_ \_ \_ \* \_** y la **\_ \_ \_ \_ \* \_ longitud del identificador de aplicación relativa** incluyen el espacio para un terminador nulo, pero las constantes en la forma: la **\_ \* \_ longitud del paquete** no incluye espacio para un terminador nulo.

 



| Constante o valor                                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**Aplicación \_ de \_ \_ \_ \_ Longitud máxima de ID. de modelo de usuario**</dt> <dt>130</dt> </dl>                  | La longitud máxima del identificador de modelo de usuario de la aplicación. Se incluye espacio para el terminador NULL.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**Aplicación \_ de \_ \_ \_ \_ Longitud mínima de ID. de modelo de usuario**</dt> <dt>21</dt> </dl>                   | La longitud mínima del identificador de modelo de usuario de la aplicación. Se incluye espacio para el terminador NULL.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud máxima**</dt> de la arquitectura <dt>7</dt> </dl>                                     | Longitud máxima de la arquitectura. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud mínima**</dt> de la arquitectura <dt>3</dt> </dl>                                     | La longitud mínima de la arquitectura. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ \_ Longitud máxima de nombre de familia**</dt> <dt>64</dt> </dl>                                      | La longitud máxima del nombre de familia. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ \_ Longitud mínima de nombre de familia**</dt> <dt>17</dt> </dl>                                      | La longitud mínima del nombre de familia. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ \_ Longitud máxima de nombre completo**</dt> <dt>127</dt> </dl>                                           | La longitud máxima del nombre completo. No se incluye ningún espacio para el terminador NULL.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**Paquete \_ de \_Nombre completo \_ min \_ longitud**</dt> <dt>30</dt> </dl>                                            | La longitud mínima del nombre completo. No se incluye ningún espacio para el terminador NULL.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud máxima de nombre**</dt> <dt>50</dt> </dl>                                                            | Longitud máxima del nombre. No se incluye ningún espacio para el terminador NULL.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud mínima de nombre**</dt> <dt>3</dt> </dl>                                                             | Longitud mínima del nombre. No se incluye ningún espacio para el terminador NULL.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud máxima de PUBLISHERID**</dt> <dt>13</dt> </dl>                                       | La longitud máxima del identificador de publicador. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud mínima de PUBLISHERID**</dt> <dt>13</dt> </dl>                                       | La longitud mínima del identificador de publicador. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud máxima del publicador**</dt> <dt>8192</dt> </dl>                                           | La longitud máxima del publicador. Por ejemplo, CN =*Publisher*. No se incluye ningún espacio para el terminador NULL.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud mínima del publicador**</dt> <dt>4</dt> </dl>                                              | La longitud mínima del publicador. No se incluye ningún espacio para el terminador NULL.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ \_ \_ Longitud máxima de ID. de aplicación relativa**</dt> <dt>65</dt> </dl> | La longitud máxima del identificador de la aplicación relativa del paquete. Se incluye espacio para el terminador NULL.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ \_ \_ Longitud mínima de identificador de aplicación relativo**</dt> <dt>2</dt> </dl>  | La longitud mínima del identificador de la aplicación relativa del paquete. Se incluye espacio para el terminador NULL.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud máxima de RESOURCEID**</dt> <dt>30</dt> </dl>                                          | La longitud máxima del identificador de recurso. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud mínima de RESOURCEID**</dt> <dt>0</dt> </dl>                                           | La longitud mínima del identificador de recurso. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud máxima de versión**</dt> <dt>23</dt> </dl>                                                   | Longitud máxima de la versión. Por ejemplo, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. No se incluye espacio para el terminador nulo/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**Paquete \_ de \_ \_ Longitud mínima**</dt> de la versión <dt>7</dt> </dl>                                                    | La longitud mínima de la versión. Por ejemplo, *x*. *x*. *x*. *x*. No se incluye ningún espacio para el terminador NULL.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>AppModel. h</dt> </dl> |



 

 





