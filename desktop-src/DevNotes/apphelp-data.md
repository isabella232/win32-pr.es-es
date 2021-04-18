---
description: Contiene información de datos de apphelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Estructura de APPHELP_DATA
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
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659345"
---
# <a name="apphelp_data-structure"></a>Estructura de datos de APPHELP \_

Contiene información de datos de apphelp.

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

**dwSeverity**
</dt> <dd>

Este parámetro puede ser APPTYPE \_ None (0).

</dd> <dt>

**dwHTMLHelpID**
</dt> <dd>

Identificador de la ayuda HTML.

</dd> <dt>

**szAppName**
</dt> <dd>

Nombre de la aplicación.

</dd> <dt>

**trExe**
</dt> <dd>

[**TAGREF**](tagref.md) del archivo ejecutable correspondiente.

</dd> <dt>

**szURL**
</dt> <dd>

La dirección URL del vínculo de apphelp en línea.

</dd> <dt>

**szLink**
</dt> <dd>

El texto del vínculo para **szURL**.

</dd> <dt>

**szAppTitle**
</dt> <dd>

Título del mensaje de apphelp.

</dd> <dt>

**szContact**
</dt> <dd>

Información de contacto del proveedor.

</dd> <dt>

**szDetails**
</dt> <dd>

Mensaje de apphelp detallado.

</dd> <dt>

**dwData**
</dt> <dd>

Datos definidos por el usuario administrados por la aplicación.

</dd> <dt>

**bSPEntry**
</dt> <dd>

Este miembro es **true** si esta entrada está en la base de datos Service Pack y **false** en caso contrario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




