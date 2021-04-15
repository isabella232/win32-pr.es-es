---
description: Abre un volumen especificado e inicializa su objeto de control de cuota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Inimétodo tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984247"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Inimétodo tialize

Abre un volumen especificado e inicializa su objeto de control de cuota.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sPath* 
</dt> <dd>

Tipo: **String**

Valor de cadena que contiene la ruta de acceso completa del volumen que se va a inicializar.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Tipo: **booleano**

Valor booleano que especifica cómo se va a abrir el volumen. Establezca *bReadWrite* en **true** para el acceso de lectura y escritura o **false** para el acceso de solo lectura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




