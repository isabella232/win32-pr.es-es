---
description: Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Método ListBackups de la clase Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ba6a3f042a6bd8f01e4bede00e22bda95ca28ebe7cc2beb33a12c6b49deba6bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589125"
---
# <a name="listbackups-method-of-the-control-class"></a>Método ListBackups de la clase Control

Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.

## <a name="syntax"></a>Sintaxis


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OriginalTimestampLow* \[ out\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración actual (si se restauró a partir de la copia de seguridad, contendrá la marca de tiempo original). Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración actual (si se restauró a partir de la copia de seguridad, contendrá la marca de tiempo original). Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*Archivos* \[ out\]
</dt> <dd>

Lista de archivos de copia de seguridad disponibles, en orden de los más nuevos a los más antiguos.

</dd> <dt>

*FilesTimestampLow* \[ out\]
</dt> <dd>

Para cada archivo de copia de seguridad, marca de tiempo de cuando se estableció su configuración. Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*FilesTimestampHigh* \[ out\]
</dt> <dd>

Para cada archivo de copia de seguridad, marca de tiempo de cuando se estableció su configuración. Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz \\ de Microsoft Windows \\ \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

