---
description: El método CreateRecord del objeto Installer devuelve un nuevo objeto Record con el número de campos solicitado.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Método Installer.CreateRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171694"
---
# <a name="installercreaterecord-method"></a>Método Installer.CreateRecord

El **método CreateRecord** del [**objeto Installer**](installer-object.md) devuelve un nuevo objeto [**Record**](record-object.md) con el número de campos solicitado.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* 
</dt> <dd>

Número necesario de campos, que pueden ser 0. El número máximo de campos de un registro se limita a 65535.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El campo 0, no uno de los campos del *recuento,* se usa normalmente para elementos orientados a registros, como cadenas de formato o códigos de operación de ejecución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




