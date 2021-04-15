---
description: La propiedad QualifierDescription de solo lectura devuelve una cadena de texto que describe el componente calificado.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Propiedad Installer. QualifierDescription
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653891"
---
# <a name="installerqualifierdescription-property"></a>Propiedad Installer. QualifierDescription

La propiedad **QualifierDescription** de solo lectura devuelve una cadena de texto que describe el componente calificado. Esta cadena traducible se crea en la columna AppData de la [tabla PublishComponent](publishcomponent-table.md) y se puede mostrar al usuario. El calificador distingue varias formas del mismo componente, como un componente que se implementa en varios lenguajes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Componentes completos](qualified-components.md)
</dt> </dl>

 

 




