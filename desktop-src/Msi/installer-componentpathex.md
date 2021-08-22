---
description: Devuelve un objeto RecordList que proporciona la ruta de acceso completa de un componente instalado especificado.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer.ComponentPathEx, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 720b10c75fcdf4a6b72f22a72d3b0860fc6089403385b0a951127f56286b6953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632628"
---
# <a name="installercomponentpathex-property"></a>Installer.ComponentPathEx, propiedad

Esta propiedad devuelve un [**objeto RecordList**](recordlist-object.md) que proporciona la ruta de acceso completa de un componente instalado especificado. Esta propiedad llama [**a MsiGetComponentPathEx.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta propiedad está disponible a partir de Windows Installer 5.0.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




