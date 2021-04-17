---
description: Recupera una máscara de bits que identifica los conjuntos de productos disponibles en el sistema. Si se llama a esta función en una aplicación que se ejecuta en el contexto de un silo de servidores, se recupera en su lugar la máscara del conjunto del silo del servidor.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Función RtlGetSuiteMask (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667971"
---
# <a name="rtlgetsuitemask-function"></a>RtlGetSuiteMask función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Recupera una máscara de bits que identifica los conjuntos de productos disponibles en el sistema. Si se llama a esta función en una aplicación que se ejecuta en el contexto de un silo de servidores, se recupera en su lugar la máscara del conjunto del silo del servidor.

## <a name="syntax"></a>Sintaxis


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Máscara de bits que identifica los conjuntos de productos disponibles en el sistema. La máscara de bits puede incluir los valores siguientes.



| Valor devuelto                                                                          | Descripción                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server se ha instalado en el sistema, pero es posible que se haya actualizado a otra versión de Windows. Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server están instalados. Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Los componentes de Microsoft BackOffice están instalados.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | Se instalan Communications Server 2003, Communications Server 2005, Communications Server 2007 o Communications Server 2007 R2.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Terminal Services está instalado. Siempre se establece este valor.<br/> Si se establece **TerminalServer** pero no se establece **SingleUserTS** , el sistema se ejecuta en modo de servidor de aplicaciones.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor. Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded está instalado.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server están instalados.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Escritorio remoto es compatible, pero solo se admite una sesión interactiva. Este valor se establece a menos que el sistema se ejecute en modo de servidor de aplicaciones.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition está instalado.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows Server 2003, Web Edition está instalado.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 o Windows Storage Server 2003 está instalado.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows Server 2003, Compute Cluster Edition está instalado.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows Home Server está instalado.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

No debe confiar solo en la marca 0x00000001 para determinar si se ha instalado Small Business Server en el sistema, ya que esta marca y la marca 0x00000020 se establecen cuando se instala este conjunto de productos. Si actualiza esta instalación a Windows Server, Standard Edition, la marca 0x00000020 se borrará, sin embargo, la marca 0x00000001 permanecerá establecida. En este caso, indica que se ha instalado Small Business Server en este sistema. Si esta instalación se actualiza aún más a Windows Server, Enterprise Edition, la marca 0x00000001 permanecerá establecida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Ntddk. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




