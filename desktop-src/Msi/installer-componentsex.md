---
description: Devuelve un objeto RecordList que enumera los componentes instalados.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Installer.ComponentsEx, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171702"
---
# <a name="installercomponentsex-property"></a>Installer.ComponentsEx, propiedad

Esta propiedad devuelve un [**objeto RecordList**](recordlist-object.md) que enumera los componentes instalados. Esta propiedad llama [**a MsiEnumComponentsEx.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta propiedad está disponible a partir de Windows Installer 5.0.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




