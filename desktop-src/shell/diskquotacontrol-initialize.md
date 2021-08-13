---
description: Abre un volumen especificado e inicializa su objeto de control de cuota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Initialize
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
ms.openlocfilehash: 0df879c626ccdac7494077f021c23a6e42b24f0df3aa780d1be8b1af8225527a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455905"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Initialize

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

Tipo: **Cadena**

Valor de cadena que contiene la ruta de acceso completa del volumen que se va a inicializar.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Tipo: **booleano**

Valor booleano que especifica cómo se va a abrir el volumen. Establezca *bReadWrite en* **TRUE para** el acceso de lectura/escritura o FALSE **para** el acceso de solo lectura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




