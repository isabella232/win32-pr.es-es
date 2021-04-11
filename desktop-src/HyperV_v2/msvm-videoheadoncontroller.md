---
description: Asocia un cabezal de vídeo al controlador de vídeo que lo incluye.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Msvm_VideoHeadOnController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156365"
---
# <a name="msvm_videoheadoncontroller-class"></a>MSVM \_ VideoHeadOnController (clase)

Asocia un cabezal de vídeo al controlador de vídeo que lo incluye.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VideoHeadOnController** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VideoHeadOnController** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

El controlador de vídeo que incluye el encabezado.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ videohead**](msvm-videohead.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

El encabezado del dispositivo de vídeo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ VideoHeadOnController** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_VIDEOHEADONCONTROLLER CIM**](cim-videoheadoncontroller.md)
</dt> <dt>

[**\_VIDEOHEADONCONTROLLER CIM**](/previous-versions//cc136950(v=vs.85))
</dt> <dt>

[Clases de vídeo](video-classes.md)
</dt> </dl>

 

