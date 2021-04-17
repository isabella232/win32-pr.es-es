---
description: La propiedad SourceListInfo del objeto Product obtiene y establece las propiedades de información de origen de un producto. Esta propiedad llama a MsiSourceListGetInfo o MsiSourceListSetInfo. Se trata de una propiedad de lectura o escritura.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Propiedad product. SourceListInfo
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
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653810"
---
# <a name="productsourcelistinfo-property"></a>Propiedad product. SourceListInfo

La propiedad **SourceListInfo** del objeto [**Product**](product-object.md) obtiene y establece las propiedades de información de origen de un producto. Esta propiedad llama a [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) o [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa). Se trata de una propiedad de lectura o escritura.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Valor de propiedad

Nombre de las propiedades de información de origen de un producto que se va a consultar o establecer. Para ver los valores posibles, consulte la sección Comentarios de este tema.

## <a name="remarks"></a>Observaciones

No se pueden establecer todas las propiedades que se pueden recuperar. El parámetro *szProperty* puede tener uno de los valores siguientes.



| Propiedad         | ¿Se puede establecer? | Significado                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | Y        | Ruta de acceso relativa a la raíz de los medios de instalación.                                                                                                                                                                                                       |
| DiskPrompt       | Y        | La plantilla de mensaje que se usa al solicitar al usuario el disco de instalación.                                                                                                                                                                                       |
| LastUsedSource   | Y        | La ubicación de origen utilizada más recientemente para el producto. Al establecer esta propiedad, Prefije la ubicación de origen con "n;" para un origen de red o "u;" para el tipo de dirección URL. Por ejemplo, "n; \\ \\ Scratch \\ Scratch \\ "y" u; https://MyServer/MyFolder/MySource ". |
| LastUsedType     | N        | "n" si el origen que se usa por última vez es una ubicación de red. "u" si el último origen utilizado era una ubicación de dirección URL. "m" si el último origen utilizado era un medio. Cadena vacía ("") si no hay ningún origen usado por última vez.                                                                   |
| PackageName      | Y        | Nombre del paquete de Windows Installer o paquete de revisión en el origen.                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Manuales**](product-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




