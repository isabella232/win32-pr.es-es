---
description: La propiedad SourceListInfo del objeto Product obtiene y establece las propiedades de información de origen de un producto. Esta propiedad llama a MsiSourceListGetInfo o MsiSourceListSetInfo. Se trata de una propiedad de lectura o escritura.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Product.SourceListInfo, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d58bc3f9eae1f953d67d2bd83b951bda1d2fe17f3f2b00cbaa9b5b7f9ad3a968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376708"
---
# <a name="productsourcelistinfo-property"></a>Product.SourceListInfo, propiedad

La **propiedad SourceListInfo** del objeto [**Product**](product-object.md) obtiene y establece las propiedades de información de origen de un producto. Esta propiedad llama [**a MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) [**o MsiSourceListSetInfo.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) Se trata de una propiedad de lectura o escritura.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Valor de propiedad

Nombre de las propiedades de información de origen de un producto que se debe consultar o establecer. Para ver los valores posibles, consulte la sección Comentarios de este tema.

## <a name="remarks"></a>Comentarios

No se pueden establecer todas las propiedades que se pueden recuperar. El *parámetro szProperty* puede ser uno de los siguientes valores.



| Propiedad         | ¿Se puede establecer? | Significado                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | Y        | Ruta de acceso relativa a la raíz del medio de instalación.                                                                                                                                                                                                       |
| DiskPrompt       | Y        | Plantilla de aviso que se usa al solicitar al usuario medios de instalación.                                                                                                                                                                                       |
| LastUsedSource   | Y        | La ubicación de origen usada más recientemente para el producto. Al establecer esta propiedad, antefiese la ubicación de origen con "n;" para un origen de red o "u;" para el tipo de dirección URL. Por ejemplo, "n; \\ \\ scratch \\ scratch \\ MySource" y "u; https://MyServer/MyFolder/MySource ". |
| LastUsedType     | N        | "n" si el último origen usado es una ubicación de red. "u" si el último origen usado era una ubicación de dirección URL. "m" si el último origen usado era un medio. Cadena vacía ("") si no hay ningún origen usado por última vez.                                                                   |
| PackageName      | Y        | Nombre del paquete Windows instalador o paquete de revisión en el origen.                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




