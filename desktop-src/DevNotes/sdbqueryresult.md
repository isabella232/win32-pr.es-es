---
description: Contiene los resultados de consultar la base de datos de correcciones de compatibilidad (shim) para obtener un ejecutable correspondiente.
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
ms.openlocfilehash: 772d30bec52758eb2ce1c39e0dcaa415c1eab25b81628e5b2865d3bdeed1b3a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815305"
---
# <a name="sdbqueryresult-structure"></a>Estructura SDBQUERYRESULT

Contiene los resultados de consultar la base de datos de correcciones de compatibilidad (shim) para obtener un ejecutable correspondiente.

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

Valores **TAGREF de** los archivos ejecutables correspondientes. Tenga en **cuenta que SDB \_ MAX \_ EXES** se define como 16.

</dd> <dt>

**adwExeFlags**
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DISABLE \_ SHIM** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABLE \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ CANCEL** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DISABLE \_ SXS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ LAYER** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DISABLE \_ DRIVER** (0x00000040)
</dt> </dl> </dd> <dt>

**atrLayers**
</dt> <dd>

Valores **TAGREF** de las capas correspondientes. Tenga en cuenta **que SDB \_ MAX \_ LAYERS** se define como 8.

</dd> <dt>

**dwLayerFlags**
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DISABLE \_ SHIM** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABLE \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ CANCEL** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DISABLE \_ SXS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ LAYER** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DISABLE \_ DRIVER** (0x00000040)
</dt> </dl> </dd> <dt>

**trApphelp**
</dt> <dd>

Valor **TAGREF** del mensaje apphelp del ejecutable correspondiente.

</dd> <dt>

**dwExeCount**
</dt> <dd>

Número de elementos de **atrExes.**

</dd> <dt>

**dwLayerCount**
</dt> <dd>

Número de elementos de **atrLayers.**

</dd> <dt>

**guidID**
</dt> <dd>

GUID del último archivo ejecutable.

</dd> <dt>

**dwFlags**
</dt> <dd>

Este parámetro puede ser uno o varios de los valores siguientes.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DISABLE \_ SHIM** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABLE \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ CANCEL** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DISABLE \_ SXS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ LAYER** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DISABLE \_ DRIVER** (0x00000040)
</dt> </dl> </dd> <dt>

**dwCustomSDBMap**
</dt> <dd>

Mapa de las bases de datos de correcciones de compatibilidad (shim) personalizadas. Los bits correspondientes se establecen si **rgGuidDB** es válido.

</dd> <dt>

**rgGuidDB**
</dt> <dd>

GUID de las bases de datos de correcciones de compatibilidad (shim). Tenga en **cuenta que \_ SDB MAX \_ SDBS** se define como 16.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




