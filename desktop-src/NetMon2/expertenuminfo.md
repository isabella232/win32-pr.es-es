---
description: La estructura EXPERTENUMINFO proporciona información sobre el experto.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Estructura EXPERTENUMINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666300"
---
# <a name="expertenuminfo-structure"></a>Estructura EXPERTENUMINFO

La estructura **EXPERTENUMINFO** proporciona información sobre el experto. Monitor de red asigna memoria para la estructura y la pasa al experto cuando llama a la función [**Register Expert**](register-expert.md) . Cuando el experto recibe la estructura, debe rellenar toda la información que Monitor de red solicitudes.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szName**
</dt> <dd>

Nombre del experto.

</dd> <dt>

**szVendor**
</dt> <dd>

Nombre del proveedor que crea el experto.

</dd> <dt>

**szDescription**
</dt> <dd>

Descripción del experto. El valor del miembro **szDescription** puede ser **null**. Si el nombre es demasiado largo, se truncará en la configuración predeterminada del visor.

</dd> <dt>

**Versión**
</dt> <dd>

El valor debe ser cero.

</dd> <dt>

**Marcas**
</dt> <dd>

Las marcas siguientes describen el experto.



| Value                                                                                                                                                                                                                                                    | Significado                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**\_marca de enumeración experta \_ \_ configurable**</dt> </dl>                                          | El experto admite llamadas al método [**Configure**](configure.md) . <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**\_visor de marcas de enumeración de expertos \_ \_ \_ privado**</dt> </dl>                                   | El experto requiere un Visor de eventos privado (no compartido). <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**\_marca de enumeración de experto \_ \_ sin \_ visor**</dt> </dl>                                                  | El experto no envía notificaciones de eventos. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**\_marca de enumeración experta \_ \_ agregarme \_ \_ a \_ RMC \_ en \_ Resumen**</dt> </dl> | Cuando el foco está en el panel de Resumen, el experto aparece en el menú contextual. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**\_marca de enumeración experta \_ \_ agregarme \_ \_ a \_ RMC \_ en \_ detalle**</dt> </dl>    | Cuando el foco está en el panel de detalles, el experto aparece en el menú contextual. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Identificador del experto. Cuando se usa la estructura **EXPERTENUMINFO** para registrar un experto, se omite el parámetro.

</dd> <dt>

**szDllName**
</dt> <dd>

Miembro privado; No use.

</dd> <dt>

**hModule**
</dt> <dd>

Miembro privado; No use.

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Miembro privado; No use.

</dd> <dt>

**pConfigProc**
</dt> <dd>

Miembro privado; No use.

</dd> <dt>

**pRunProc**
</dt> <dd>

Miembro privado; No use.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




