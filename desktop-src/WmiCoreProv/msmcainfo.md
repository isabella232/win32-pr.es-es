---
description: Una clase base abstracta de la que se derivan todas las clases de datos del proveedor machine check architecture (MCA), como MSMCAInfo \_ RawMCAData. Esta clase solo está disponible en sistemas de 64 Windows bits.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568104"
---
# <a name="msmcainfo-class"></a>Clase MSMCAInfo

La clase **MSMCAInfo** es una clase base abstracta de la que se derivan todas las clases de datos del proveedor Machine Check Architecture (MCA), como [**MSMCAInfo \_ RawMCAData.**](msmcainfo-rawmcadata.md) El proveedor de MCA también tiene clases de eventos, derivadas de [**WMIEvent**](wmievent.md). Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Members

La **clase MSMCAInfo** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**Encabezado MSMCAEvent \_**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




