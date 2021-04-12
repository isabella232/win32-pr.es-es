---
description: Describe cómo leer un documento XPS existente de un archivo en un OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Leer un documento XPS en un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361243"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Leer un documento XPS en un OM XPS

Describe cómo leer un documento XPS existente de un archivo en un OM XPS.

Para crear un OM XPS a partir de un documento XPS, llame al método [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .

Antes de usar estos ejemplos de código en el programa, lea la declinación de responsabilidades en [las tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Ejemplo de código

En el ejemplo de código siguiente se da por supuesto que la inicialización descrita en [Initialize an XPS OM](xps-object-model-initialization.md) se ha realizado correctamente.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Para crear un OM XPS a partir de un documento XPS que está almacenado como un flujo, llame a [**IXpsOMObjectFactory:: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).

## <a name="remarks"></a>Observaciones

Si escribe un OM XPS inmediatamente después de haber leído un paquete XPS en él, es posible que se pierda o cambie parte del contenido original.

En la tabla siguiente se enumeran algunos de los cambios que se pueden producir en este caso:

| Característica de documento                      | Acción                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Firmas digitales<br/>         | Quitado del documento<br/>                               |
| Elemento DiscardControl<br/>        | Quitado del documento<br/>                               |
| Partes de documentos externos<br/>     | Quitado del documento<br/>                               |
| Marcado de FixedPage<br/>           | Modificado desde el original<br/>                              |
| Marcado del Diccionario de recursos<br/> | Modificado desde el original, si se establece la marca de optimización<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Navegar por el OM de XPS](navigate-the-xps-om.md)
</dt> <dt>

[Escribir texto en un OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Dibujar gráficos en un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Colocar imágenes en un OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Inicializar un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[API de empaquetado](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Referencia de la API de documentos XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

