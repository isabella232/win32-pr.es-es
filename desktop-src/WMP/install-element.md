---
title: Elemento Install
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento Install especifica los valores usados por Reproductor de Windows Media para instalar un almacén en línea.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Install Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249603"
---
# <a name="install-element"></a>Elemento Install

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento Install** especifica los valores usados por Reproductor de Windows Media para instalar un almacén en línea.

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obligatorio)
</dt> <dd>

Dirección URL completa de un archivo con una extensión .txt nombre de archivo que Reproductor de Windows Media para mostrar un Contrato de licencia de usuario final (CLUF). Este archivo debe codificarse en formato ANSI.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obligatorio)
</dt> <dd>

Dirección URL completa de un paquete, con una .cab de nombre de archivo, que se usa para instalar el almacén en línea. El paquete y todos los módulos de código del paquete deben estar firmados. Para obtener información sobre la firma de código, vea [Introducción a la firma de](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) código en MSDN Library.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obligatorio)
</dt> <dd>

Dirección URL completa de una página web que contiene información de directiva de privacidad para la tienda en línea.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obligatorio)
</dt> <dd>

Nombre del archivo EXE o INF que se ejecutará. Este archivo debe estar incluido en el archivo CAB especificado por el **atributo CodeURL.**

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (opcional)
</dt> <dd>

Cadena de línea de comandos que se pasa a la aplicación especificada por el **atributo InstallApp.** Este atributo solo es aplicable cuando el valor de **InstallApp** especifica un archivo ejecutable.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (obligatorio para el tipo 1, omitido para el tipo 2)
</dt> <dd>

Dirección URL completa del catálogo compilado de la tienda en línea.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Si falta alguno de los atributos necesarios o no está disponible, Reproductor de Windows Media programa de instalación no intentará descargar e instalar el código del proveedor de la tienda en línea. El programa de instalación configurará los valores predeterminados sin conexión como se especifica en el **documento ServiceInfo.** **ServiceInfo** se puede usar cuando no está conectado a Internet pasando el nombre del proveedor predeterminado y la **información de ServiceInfo** como parámetros de línea de comandos. Consulte [Redistributing Reproductor de Windows Media Software para](redistributing-windows-media-player-software.md) obtener más información sobre las opciones de la línea de comandos.

> [!Note]  
> El uso de este elemento requiere que firme un contrato de redistribución con Microsoft. Póngase en contacto con su representante empresarial para obtener más información.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

