---
description: Una clase base abstracta de la que se derivan todas las clases de datos del proveedor de la arquitectura de comprobación de equipo (MCA), como MSMCAInfo \_ RawMCAData. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Clase MSMCAInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082108"
---
# <a name="msmcainfo-class"></a>Clase MSMCAInfo

La clase **MSMCAInfo** es una clase base abstracta de la que se derivan todas las clases de datos del proveedor de la arquitectura de comprobación de equipo (MCA), como [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md). El proveedor de MCA también tiene clases de eventos, que se derivan de [**WMIEvent**](wmievent.md). Esta clase solo está disponible en sistemas Windows de 64 bits.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Miembros

La clase **MSMCAInfo** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**\_Encabezado MSMCAEvent**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




