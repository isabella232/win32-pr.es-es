---
description: Obtenga información sobre el elemento configurable por el usuario DocumentBannerSheet. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548773"
---
# <a name="documentbannersheet"></a>DocumentBannerSheet

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe la hoja de banners que se va a generar para un documento determinado. La hoja de banners debe generarse en el valor predeterminado PageMediaSize , utilizando el valor predeterminado PageMediaType. La hoja de banners también debe aislarse del resto del documento. Esto significa que las opciones de finalización o procesamiento de documentos (como DocumentDuplex, DocumentStaple o DocumentBinding) no deben incluir la hoja de banners. La hoja de banners puede o no estar aislada del resto del trabajo. Esto significa que cualquier opción de finalización o procesamiento del trabajo puede incluir la hoja de banners del documento. La hoja de banners debe aparecer como la primera hoja del documento.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento <br/>   | Característica<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prefijo de ámbito <br/> | Documento<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Notas <br/>          | Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante. Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento. Esta configuración es específica de XPS. <br/> Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL. Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.<br/> |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                               | Tipo de datos         | Unidad                   | Valores admitidos                                                                                                                                                                      | Resumen                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caracteres <br/> | Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción<br/>                                            |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>         | True, False<br/>                                                                                                                                                                | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




