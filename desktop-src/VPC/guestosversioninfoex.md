---
title: Estructura GUESTOSVERSIONINFOEX (VPCCOMInterfaces.h)
description: Contiene información de versión del sistema operativo para el sistema operativo invitado.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX estructura Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848196448c2bd6f021d85f7c13972e81664dd60a0e4a0bbbd2e05ef3455aade7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056913"
---
# <a name="guestosversioninfoex-structure"></a>ESTRUCTURA GUESTOSVERSIONINFOEX

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Contiene información de versión del sistema operativo para el sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwOSVersionInfoSize**
</dt> <dd>

Tamaño de esta estructura de datos, en bytes. Establezca este miembro en `sizeof(GUESTOSVERSIONINFOEX)` .

</dd> <dt>

**dwMajorVersion**
</dt> <dd>

Número de versión principal.

</dd> <dt>

**dwMinorVersion**
</dt> <dd>

Número de versión secundaria.

</dd> <dt>

**dwBuildNumber**
</dt> <dd>

Número de compilación.

</dd> <dt>

**dwPlatformId**
</dt> <dd>

Plataforma del sistema operativo. Este miembro puede ser **VER \_ PLATFORM \_ WIN32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Cadena terminada en NULL, como "Service Pack 3", que indica el Service Pack más reciente instalado en el sistema. Si no se ha instalado ningún Service Pack, la cadena está vacía.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Número de versión principal del Service Pack más reciente instalado.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

Número de versión secundaria del Service Pack más reciente instalado.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Máscara de bits que identifica los conjuntos de productos disponibles en el sistema. Este miembro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**VER \_ SUITE \_ BACKOFFICE**</dt> <dt>0x00000004</dt> </dl>                                            | Los componentes de Microsoft BackOffice están instalados.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**VER \_ HOJA \_ SUITE**</dt> <dt>0x00000400</dt> </dl>                                                           | Windows Server 2003, Web Edition está instalado.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**VER \_ SUITE \_ COMPUTE \_ SERVER**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition está instalado.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**VER \_ SUITE \_ DATACENTER**</dt> <dt>0x00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows Datacenter Server 2000 está instalado.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**VER \_ SUITE \_ ENTERPRISE**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows Advanced Server 2000 está instalado. Consulte la sección Comentarios para obtener más información sobre esta marca de bits.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**VER \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded está instalado.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**VER \_ SUITE \_ PERSONAL**</dt> <dt>0x00000200</dt> </dl>                                                  | Windows Vista Home Premium, Windows Vista Home Basic o Windows xp Home Edition está instalado.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**VER \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Escritorio remoto se admite, pero solo se admite una sesión interactiva. Este valor se establece a menos que el sistema se ejecute en modo de servidor de aplicaciones.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**VER \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server se instaló una vez en el sistema, pero puede que se haya actualizado a otra versión de Windows. Consulte la sección Comentarios para obtener más información sobre esta marca de bits.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**VER \_ SUITE \_ SMALLBUSINESS \_ RESTRICTED**</dt> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor. Consulte la sección Comentarios para obtener más información sobre esta marca de bits.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**VER \_ SUITE \_ STORAGE \_ SERVER**</dt> <dt>0x00002000</dt> </dl>                               | Windows Storage Server 2003 R2 o Windows Storage Server 2003 está instalado.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**VER \_ TERMINAL \_ SUITE**</dt> <dt>0x00000010</dt> </dl>                                                  | Terminal Services está instalado. Este valor siempre se establece.<br/> Si **se establece VER SUITE \_ \_ TERMINAL** pero NO SE ESTABLECE **VER SUITE \_ \_ SINGLEUSERTS,** el sistema se ejecuta en modo de servidor de aplicaciones.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**VER \_ SUITE \_ WH \_ SERVER**</dt> <dt>0x00008000</dt> </dl>                                              | Windows El servidor principal está instalado.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Cualquier información adicional sobre el sistema. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**VER \_ CONTROLADOR \_ DE \_ DOMINIO NT**</dt> <dt>0x0000002</dt> </dl> | El sistema es un controlador de dominio y el sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**VER \_ NT \_ SERVER**</dt> <dt>0x0000003</dt> </dl>                                   | El sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/> Tenga en cuenta que un servidor que también es un controlador de dominio se notifica como CONTROLADOR DE **DOMINIO DE VER \_ NT, \_ \_** no **COMO SERVIDOR DE VER \_ NT \_**.<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**VER \_ NT \_ WORKSTATION**</dt> <dt>0x0000001</dt> </dl>                    | El sistema operativo se Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

