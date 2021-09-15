---
title: Buffer (objeto)
description: Buffer (objeto)
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows SDK de formato multimedia, objetos de búfer
- Formato de sistemas avanzados (ASF), objetos de búfer
- ASF (formato de sistemas avanzados), objetos de búfer
- objects,buffer objects
- objetos de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467105"
---
# <a name="buffer-object"></a>Buffer (objeto)

Un objeto de búfer se usa para contener ejemplos y entregarlos entre los objetos del SDK Windows Media Format y la aplicación. Al escribir un archivo, se pasan los ejemplos de entrada al escritor mediante objetos de búfer. Al leer un archivo, el objeto de lector o el objeto de lector sincrónico proporciona ejemplos a la aplicación en objetos de búfer.

Para escribir ejemplos en un archivo, puede crear un objeto de búfer mediante el [**método IWMWriter::AllocateSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) Para leer ejemplos, el objeto lector y el objeto de lector sincrónico crean objetos de búfer internamente. Si lo decide, puede asignar sus propios objetos de búfer para la lectura de archivos mediante [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) o [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).

Todos los objetos de búfer admiten las interfaces siguientes.



| Interfaz                          | Descripción                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | Controla y proporciona acceso al búfer.                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | Sin implementar.                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | Admite propiedades de búfer, que se usan para las extensiones de unidad de datos. |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | Enumera las propiedades del búfer.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




