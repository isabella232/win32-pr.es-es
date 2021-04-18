---
description: PStore usa las siguientes constantes.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: PStore (constantes) (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670869"
---
# <a name="pstore-constants"></a>PStore (constantes)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

PStore usa las siguientes constantes.

Códigos de error de almacenamiento protegido



| Constante o valor                                                                                                                                                                                                                               | Descripción                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**Archivo pst \_ E \_ Aceptar**</dt> <dt>0x00000000L</dt> </dl>                             | La operación se realizó correctamente.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**Archivo pst \_ El \_ tipo E \_ existe**</dt> <dt>0x800C0004L</dt> </dl> | El elemento de datos ya existe en el almacenamiento protegido. <br/> |



Valores de la cláusula de acceso



| Constante o valor                                                                                                                                                                                                                                      | Descripción                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**Archivo pst \_ AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | Apunta a una estructura de [**\_ AUTHENTICODEDATA de PST**](pst-authenticodedata.md) .<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **\_ \_ Comprobación binaria de PST**</dt> <dt>2</dt> </dl>                   | Apunta a una estructura de **\_ BINARYCHECKDATA de PST** .<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**Archivo pst \_ \_Descriptor de seguridad**</dt> <dt>4</dt> </dl> | Apunta a un descriptor de seguridad de Windows válido. <br/>                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
