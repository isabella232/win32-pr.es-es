---
description: Contiene los resultados de la consulta de la base de datos de correcciones de compatibilidad (shim) para un ejecutable coincidente.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Estructura SDBQUERYRESULT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998206"
---
# <a name="sdbqueryresult-structure"></a>Estructura SDBQUERYRESULT

Contiene los resultados de la consulta de la base de datos de correcciones de compatibilidad (shim) para un ejecutable coincidente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**atrExes**
</dt> <dd>

Los valores **TAGREF** de los archivos ejecutables coincidentes. Tenga en cuenta que los archivos **\_ \_ exe Max de SDB** se definen como 16.

</dd> <dt>

**adwExeFlags**
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)
</dt> </dl> </dd> <dt>

**atrLayers**
</dt> <dd>

Los valores de **TAGREF** de las capas coincidentes. Tenga en cuenta que los **\_ \_ niveles máximos de SDB** están definidos como 8.

</dd> <dt>

**dwLayerFlags**
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)
</dt> </dl> </dd> <dt>

**trApphelp**
</dt> <dd>

El valor **TAGREF** del mensaje de apphelp del ejecutable correspondiente.

</dd> <dt>

**dwExeCount**
</dt> <dd>

Número de elementos de **atrExes**.

</dd> <dt>

**dwLayerCount**
</dt> <dd>

Número de elementos de **atrLayers**.

</dd> <dt>

**guidID**
</dt> <dd>

GUID del último archivo ejecutable.

</dd> <dt>

**dwFlags**
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)
</dt> </dl> </dd> <dt>

**dwCustomSDBMap**
</dt> <dd>

Una asignación de las bases de datos de corrección de compatibilidad (shim) personalizadas. Los bits correspondientes se establecen si **rgGuidDB** es válido.

</dd> <dt>

**rgGuidDB**
</dt> <dd>

Los GUID de las bases de datos de correcciones de compatibilidad (shim). Tenga en cuenta que **SDB \_ Max \_ SDBS** se define como 16.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




