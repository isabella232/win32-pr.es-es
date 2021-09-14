---
description: La propiedad SourceListInfo del objeto Patch obtiene y establece las propiedades de información de origen de una revisión. Esta propiedad llama a MsiSourceListGetInfo o MsiSourceListSetInfo. Se trata de una propiedad de lectura o escritura.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Patch.SourceListInfo, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173689"
---
# <a name="patchsourcelistinfo-property"></a>Patch.SourceListInfo, propiedad

La **propiedad SourceListInfo** del objeto [**Patch**](patch-object.md) obtiene y establece las propiedades de información de origen de una revisión. Esta propiedad llama [**a MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) [**o MsiSourceListSetInfo.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) Se trata de una propiedad de lectura o escritura.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a>Valor de propiedad

Nombre de las propiedades de información de origen de una revisión que se consulta o establece. Para ver los valores posibles, consulte la sección Comentarios de este tema.

## <a name="remarks"></a>Observaciones

No se pueden establecer todas las propiedades que se pueden recuperar. El *parámetro szProperty* puede ser uno de los siguientes valores.



| Propiedad         | ¿Se puede establecer? | Significado                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | Y        | Ruta de acceso relativa a la raíz del medio de instalación.                                                                                                                                                                                                          |
| DiskPrompt       | Y        | Plantilla de aviso que se usa al solicitar al usuario medios de instalación.                                                                                                                                                                                          |
| LastUsedSource   | Y        | La ubicación de origen usada más recientemente para la revisión. Al establecer esta propiedad, antefiese la ubicación de origen con "n;" para un origen de red o "u;" para el tipo de dirección URL. Por ejemplo, use "n; \\ \\ scratch \\ scratch \\ test" o "u; https://microsoft.com/Patches/Office/SP1 ". |
| LastUsedType     | No        | "n" si el último origen usado es una ubicación de red. "u" si el último origen usado era una ubicación de dirección URL. "m" si el último origen usado era un medio. Cadena vacía ("") si no hay ningún origen usado por última vez.                                                                      |
| PackageName      | Y        | Nombre del paquete Windows instalador o paquete de revisión en el origen.                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




