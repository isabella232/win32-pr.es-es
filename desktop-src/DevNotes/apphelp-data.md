---
description: Contiene información de datos de Apphelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: APPHELP_DATA estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: e9aab48760af45772cf77b4f943144ceab4104ebfd762c8ec7402caf1de8cfec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103765"
---
# <a name="apphelp_data-structure"></a>ESTRUCTURA DE DATOS DE APPHELP \_

Contiene información de datos de Apphelp.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwFlags**
</dt> <dd>

Este parámetro puede ser uno de los siguientes valores.

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

**dwSeverity**
</dt> <dd>

Este parámetro puede ser APPTYPE \_ NONE (0).

</dd> <dt>

**dwHTMLHelpID**
</dt> <dd>

Identificador de Ayuda HTML.

</dd> <dt>

**szAppName**
</dt> <dd>

Nombre de la aplicación.

</dd> <dt>

**trExe**
</dt> <dd>

TAGREF [**del**](tagref.md) archivo ejecutable correspondiente.

</dd> <dt>

**szURL**
</dt> <dd>

Dirección URL del vínculo en línea de Apphelp.

</dd> <dt>

**szLink**
</dt> <dd>

Texto del vínculo para **szURL.**

</dd> <dt>

**szAppTitle**
</dt> <dd>

Título del mensaje de Apphelp.

</dd> <dt>

**szContact**
</dt> <dd>

Información de contacto del proveedor.

</dd> <dt>

**szDetails**
</dt> <dd>

El mensaje de Apphelp detallado.

</dd> <dt>

**dwData**
</dt> <dd>

Datos definidos por el usuario administrados por la aplicación.

</dd> <dt>

**bSPEntry**
</dt> <dd>

Este miembro es **TRUE si** esta entrada está en la base de datos de Service Pack y **FALSE en** caso contrario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




