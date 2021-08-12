---
title: Constantes de identidad (AppModel.h)
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
ms.openlocfilehash: 4590e62397ac069cb0fc9661f615288c2d8df36ba41304fff71e4ef0293f9f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552217"
---
# <a name="identity-constants"></a>Constantes de identidad

Especifica la longitud de las cadenas para los campos de identidad del paquete. La longitud se mide en caracteres y puede incluir o no espacio para el terminador NULL.

> [!Note]  
> Las constantes con el formato: APPLICATION **\_ USER MODEL ID \_ \_ \_ \* \_ LENGTH** y PACKAGE RELATIVE APPLICATION **ID \_ \_ \_ \_ \* \_ LENGTH** incluyen espacio para un terminador NULL, pero las constantes con el formato: PACKAGE **\_ \* \_ LENGTH** no incluyen espacio para un terminador NULL.

 



| Constante o valor                                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**APLICACIÓN \_ USER \_ MODEL ID MAX \_ \_ \_ LENGTH**</dt> <dt>130</dt> </dl>                  | Longitud máxima del identificador del modelo de usuario de la aplicación. Se incluye espacio para el terminador NULL.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**APLICACIÓN \_ ID. \_ DE MODELO DE USUARIO LONGITUD \_ \_ \_ MÍNIMA**</dt> <dt>21</dt> </dl>                   | Longitud mínima del identificador de modelo de usuario de la aplicación. Se incluye espacio para el terminador NULL.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÁXIMA \_ DE ARQUITECTURA**</dt> <dt>7</dt> </dl>                                     | Longitud máxima de la arquitectura. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**PACKAGE \_ ARQUITECTURA \_ LONGITUD \_ MÍNIMA**</dt> <dt>3</dt> </dl>                                     | Longitud mínima de la arquitectura. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**PACKAGE \_ FAMILY \_ NAME \_ MAX \_ LENGTH**</dt> <dt>64</dt> </dl>                                      | Longitud máxima del nombre de familia. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**PACKAGE \_ FAMILY \_ NAME \_ MIN \_ LENGTH**</dt> <dt>17</dt> </dl>                                      | Longitud mínima del nombre de familia. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**PACKAGE \_ NOMBRE \_ COMPLETO \_ LONGITUD \_ MÁXIMA**</dt> <dt>127</dt> </dl>                                           | Longitud máxima del nombre completo. No se incluye ningún espacio para el terminador NULL.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**PACKAGE \_ NOMBRE \_ COMPLETO \_ LONGITUD \_ MÍNIMA**</dt> <dt>30</dt> </dl>                                            | Longitud mínima del nombre completo. No se incluye ningún espacio para el terminador NULL.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÁXIMA \_ DE NOMBRE**</dt> <dt>50</dt> </dl>                                                            | Longitud máxima del nombre. No se incluye ningún espacio para el terminador NULL.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**PACKAGE \_ NOMBRE \_ LONGITUD \_ MÍNIMA**</dt> <dt>3</dt> </dl>                                                             | Longitud mínima del nombre. No se incluye ningún espacio para el terminador NULL.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**PACKAGE \_ PUBLISHERID \_ MAX \_ LENGTH**</dt> <dt>13</dt> </dl>                                       | Longitud máxima del identificador del publicador. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**PACKAGE \_ PUBLISHERID \_ LONGITUD \_ MÍNIMA**</dt> <dt>13</dt> </dl>                                       | Longitud mínima del identificador del publicador. No se incluye ningún espacio para el terminador NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÁXIMA \_ DEL PUBLICADOR**</dt> <dt>8192</dt> </dl>                                           | Longitud máxima del publicador. Por ejemplo, CN=*publicador*. No se incluye ningún espacio para el terminador NULL.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÍNIMA \_ DEL PUBLICADOR**</dt> <dt>4</dt> </dl>                                              | Longitud mínima del publicador. No se incluye ningún espacio para el terminador NULL.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÁXIMA DEL IDENTIFICADOR DE APLICACIÓN \_ \_ \_ RELATIVA**</dt> <dt>65</dt> </dl> | Longitud máxima del identificador de aplicación relativa del paquete. Se incluye espacio para el terminador NULL.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÍNIMA DEL IDENTIFICADOR DE APLICACIÓN \_ \_ \_ RELATIVA**</dt> <dt>2</dt> </dl>  | Longitud mínima del identificador de aplicación relativa del paquete. Se incluye espacio para el terminador NULL.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**PACKAGE \_ RESOURCEID \_ MAX \_ LENGTH**</dt> <dt>30</dt> </dl>                                          | Longitud máxima del identificador de recurso. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**PACKAGE \_ RESOURCEID \_ LONGITUD \_ MÍNIMA**</dt> <dt>0</dt> </dl>                                           | Longitud mínima del identificador de recurso. No se incluye ningún espacio para el terminador NULL.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**PACKAGE \_ LONGITUD \_ MÁXIMA \_ DE VERSIÓN**</dt> <dt>23</dt> </dl>                                                   | Longitud máxima de la versión. Por ejemplo, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. No se incluye ningún espacio para el terminador NULL/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**PACKAGE \_ VERSIÓN \_ MÍNIMA \_ LONGITUD**</dt> <dt>7</dt> </dl>                                                    | Longitud mínima de la versión. Por ejemplo, *x*. *x*. *x*. *x*. No se incluye ningún espacio para el terminador NULL.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>AppModel.h</dt> </dl> |



 

 





