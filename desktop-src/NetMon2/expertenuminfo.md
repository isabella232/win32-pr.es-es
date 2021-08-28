---
description: La estructura EXPERTENUMINFO proporciona información sobre el experto.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Estructura EXPERTENUMINFO (Netmon.h)
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
ms.openlocfilehash: 46942f1140cbb5f74685b16e468b68b85221deceeae2509a9d0676261898e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939042"
---
# <a name="expertenuminfo-structure"></a>ESTRUCTURA EXPERTENUMINFO

La **estructura EXPERTENUMINFO** proporciona información sobre el experto. Monitor de red asigna memoria para la estructura y la pasa al experto cuando llama a la [**función Register Expert.**](register-expert.md) Cuando el experto recibe la estructura, debe rellenar toda la información que Monitor de red solicitudes.

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

Descripción del experto. El valor del **miembro szDescription** puede ser **NULL.** Si el nombre es demasiado largo, se trunca en la configuración predeterminada del visor.

</dd> <dt>

**Versión**
</dt> <dd>

El valor debe ser cero.

</dd> <dt>

**Marcas**
</dt> <dd>

Las marcas siguientes describen al experto.



| Value                                                                                                                                                                                                                                                    | Significado                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**MARCA \_ DE \_ ENUMERACIÓN DE EXPERTO \_ CONFIGURABLE**</dt> </dl>                                          | El experto admite llamadas al [**método**](configure.md) Configure. <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**VISOR \_ DE MARCAS DE \_ \_ ENUMERACIÓN EXPERTO \_ PRIVADO**</dt> </dl>                                   | El experto requiere una cuenta privada (no compartida) Visor de eventos. <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**MARCA \_ DE ENUMERACIÓN \_ EXPERTO SIN \_ \_ VISOR**</dt> </dl>                                                  | El experto no envía notificaciones de eventos. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG ADD ME TO \_ \_ RMC IN SUMMARY (AGREGARME A \_ \_ RMC EN \_ \_ RESUMEN)**</dt> </dl> | Cuando el foco está en el panel de resumen, el experto aparece en el menú contextual. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**MARCA \_ ENUM \_ EXPERT ADD ME TO \_ \_ \_ \_ RMC IN \_ \_ DETAIL**</dt> </dl>    | Cuando el foco está en el panel de detalles, el experto aparece en el menú contextual. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Controle al experto. Cuando se **usa la estructura EXPERTENUMINFO** para registrar un experto, se omite el parámetro .

</dd> <dt>

**szDllName**
</dt> <dd>

Miembro privado; no se usan.

</dd> <dt>

**hModule**
</dt> <dd>

Miembro privado; no se usan.

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Miembro privado; no se usan.

</dd> <dt>

**pConfigProc**
</dt> <dd>

Miembro privado; no se usan.

</dd> <dt>

**pRunProc**
</dt> <dd>

Miembro privado; no se usan.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




