---
description: PStore usa las siguientes constantes.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Constantes de PStore (Pstore.h)
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
ms.openlocfilehash: 69a82241e8f270389c5385143e83973d380f5671e30e2086749a75c984670cf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386045"
---
# <a name="pstore-constants"></a>Constantes de PStore

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

PStore usa las siguientes constantes.

Códigos de error Storage protección



| Constante o valor                                                                                                                                                                                                                               | Descripción                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**PST \_ E \_ OK**</dt> <dt>0x00000000L</dt> </dl>                             | La operación se realizó correctamente.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**PST \_ E \_ TYPE \_ EXISTS**</dt> <dt>0x800C0004L</dt> </dl> | El elemento de datos ya existe en el almacenamiento protegido. <br/> |



Valores de cláusula de acceso



| Constante o valor                                                                                                                                                                                                                                      | Descripción                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**PST \_ AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | Apunta a una [**estructura \_ AUTHENTICODEDATA de PST.**](pst-authenticodedata.md)<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **PST \_ BINARY \_ CHECK**</dt> <dt>2</dt> </dl>                   | Apunta a una **estructura \_ BINARYCHECKDATA de PST.**<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**PST \_ \_DESCRIPTOR DE SEGURIDAD**</dt> <dt>4</dt> </dl> | Apunta a un descriptor de Windows válido. <br/>                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
