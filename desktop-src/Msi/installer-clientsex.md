---
description: Devuelve un objeto RecordList que enumera los productos que usan un componente instalado especificado.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Installer.ClientsEx, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171734"
---
# <a name="installerclientsex-property"></a>Installer.ClientsEx, propiedad

Esta propiedad devuelve un [**objeto RecordList**](recordlist-object.md) que enumera los productos que usan un componente instalado especificado. Esta propiedad llama [**a MsiEnumClientsEx.**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)

**[Windows Installer 4.5 o versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta propiedad está disponible a partir de Windows Installer 5.0.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ClientsEx
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

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




