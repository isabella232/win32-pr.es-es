---
description: Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Método ListBackups de la clase control
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
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152775"
---
# <a name="listbackups-method-of-the-control-class"></a>Método ListBackups de la clase control

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

*OriginalTimestampLow* \[ enuncia\]
</dt> <dd>

La marca de tiempo de cuando se estableció la configuración actual (si se restaura a partir de una copia de seguridad, contendrá la marca de tiempo original). Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ enuncia\]
</dt> <dd>

La marca de tiempo de cuando se estableció la configuración actual (si se restaura a partir de una copia de seguridad, contendrá la marca de tiempo original). Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Archivos* \[ de enuncia\]
</dt> <dd>

La lista de archivos de copia de seguridad disponibles, en orden de la más reciente a la más antigua.

</dd> <dt>

*FilesTimestampLow* \[ enuncia\]
</dt> <dd>

Para cada archivo de copia de seguridad, la marca de tiempo de cuando se estableció su configuración. Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*FilesTimestampHigh* \[ enuncia\]
</dt> <dd>

Para cada archivo de copia de seguridad, la marca de tiempo de cuando se estableció su configuración. Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz de \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

