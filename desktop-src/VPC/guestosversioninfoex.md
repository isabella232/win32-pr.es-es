---
title: Estructura GUESTOSVERSIONINFOEX (VPCCOMInterfaces. h)
description: Contiene información de versión del sistema operativo para el sistema operativo invitado.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX estructura virtual PC
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
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150485"
---
# <a name="guestosversioninfoex-structure"></a>Estructura GUESTOSVERSIONINFOEX

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Plataforma del sistema operativo. Este miembro puede ser **la \_ plataforma ver \_ Win32 \_ NT** (2).

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Una cadena terminada en null, como "Service Pack 3", que indica el último Service Pack instalado en el sistema. Si no se ha instalado ningún Service Pack, la cadena está vacía.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Número de versión principal del Service Pack más reciente instalado.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

El número de versión secundaria del último Service Pack instalado.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Máscara de máscara que identifica los conjuntos de productos disponibles en el sistema. Este miembro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**Ver \_ SUITE \_ BackOffice**</dt> <dt>0x00000004</dt> </dl>                                            | Los componentes de Microsoft BackOffice están instalados.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**Ver \_ PAQUETE \_**</dt> de la hoja <dt>0x00000400</dt> </dl>                                                           | Windows Server 2003, Web Edition está instalado.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**Ver \_ CONJUNTO de \_ \_ servidores de proceso**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition está instalado.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**Ver \_ CONJUNTO de \_ centros**</dt> de <dt>0x00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server están instalados.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server están instalados. Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded está instalado.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**Ver \_ 0x00000200 \_ personal de Suite**</dt> <dt></dt> </dl>                                                  | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition está instalado.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Escritorio remoto es compatible, pero solo se admite una sesión interactiva. Este valor se establece a menos que el sistema se ejecute en modo de servidor de aplicaciones.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**Ver \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server se ha instalado en el sistema, pero es posible que se haya actualizado a otra versión de Windows. Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**Ver \_ SUITE de uso \_ \_ restringido de SMALLBUSINESS**</dt> <dt></dt> </dl> | Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor. Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**Ver \_ SUITE de \_ Storage \_ Server**</dt> <dt>0x00002000</dt> </dl>                               | Windows Storage Server 2003 R2 o Windows Storage Server 2003 están instalados.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**Ver \_ CONJUNTO de \_ terminales**</dt> <dt>0x00000010</dt> </dl>                                                  | Terminal Services está instalado. Siempre se establece este valor.<br/> Si se establece el **\_ \_ terminal de versión del paquete** , pero no se establece **Ver \_ Suite \_ SINGLEUSERTS** , el sistema se ejecuta en modo de servidor de aplicaciones.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**Ver \_ SUITE \_ qu \_ Server**</dt> <dt>0x00008000</dt> </dl>                                              | Windows Home Server está instalado.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Cualquier información adicional sobre el sistema. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**Ver \_ \_ \_ Controlador de dominio NT**</dt> <dt>0x0000002</dt> </dl> | El sistema es un controlador de dominio y el sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**Ver \_ 0x0000003 de NT \_ Server**</dt> <dt></dt> </dl>                                   | El sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/> Tenga en cuenta que un servidor que también es un controlador de dominio se indica como controlador de dominio de NT de ver, no como **\_ \_ servidor de NT**. **\_ \_ \_**<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**Ver \_ NT \_ Workstation**</dt> <dt>0x0000001</dt> </dl>                    | El sistema operativo es Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

