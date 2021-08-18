---
description: La propiedad QualifierDescription de solo lectura devuelve una cadena de texto que describe el componente completo.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Installer.QualifierDescription, propiedad
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
ms.openlocfilehash: c226f00d7f95b4585fa4a0713fb281011079cdc35c4e421254beec75db84d7db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763585"
---
# <a name="installerqualifierdescription-property"></a>Installer.QualifierDescription, propiedad

La propiedad **QualifierDescription** de solo lectura devuelve una cadena de texto que describe el componente completo. Esta cadena localizable se crea en la columna AppData de la [tabla PublishComponent](publishcomponent-table.md) y se puede mostrar al usuario. El calificador distingue varias formas del mismo componente, como un componente que se implementa en varios idiomas.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Componentes calificados](qualified-components.md)
</dt> </dl>

 

 




