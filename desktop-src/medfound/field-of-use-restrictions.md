---
description: Campo de restricciones de uso
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Campo de restricciones de uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16f57de7642fa789a08c886a32bf906faffb72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360093"
---
# <a name="field-of-use-restrictions"></a>Campo de restricciones de uso

> [!Note]  
> Este tema se aplica a Windows 7 o posterior.

 

Una restricción *de campo de uso* es una disposición que limita el modo en que se puede usar una licencia para una tecnología determinada.

Media Foundation proporciona un mecanismo para aplicar las restricciones de campo de uso en Media Foundation transformaciones (MFTs), especialmente los códecs. Este mecanismo requiere que el MFT bloquee su propio uso por parte de las aplicaciones hasta que la aplicación haya realizado un protocolo de enlace con la MFT. Media Foundation no define el protocolo de enlace, normalmente implicaría algún tipo de intercambio criptográfico.

### <a name="registration-and-enumeration"></a>Registro y enumeración

Si una MFT tiene restricciones de campo de uso, establezca la marca **de \_ enumeración \_ \_ FIELDOFUSE de MFT** al registrar la MFT. Esta marca se aplica a las siguientes API de registro de MFT:

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

De forma predeterminada, los MFTs registrados con esta marca se excluyen de los resultados de la enumeración. Para enumerar MFTs con restricciones de campo de uso, llame a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) y especifique la marca de **\_ enumeración de MFT \_ \_ FIELDOFUSE** Flag en el parámetro *Flags* . En el siguiente diagrama se muestra este proceso.

![diagrama que muestra MFT y una aplicación que envía datos al registro](images/mft-fou01.gif)

La función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) siempre excluye cualquier MFTs que tenga restricciones de campo de uso.

### <a name="unlocking-the-mft"></a>Desbloqueo de MFT

Para usar una MFT con restricciones de campo de uso, realice los pasos siguientes:

1.  La aplicación implementa la interfaz [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .
2.  El método [**IMFFieldOfUseMFTUnlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) toma un puntero a la interfaz **IUnknown** de MFT.
3.  En el método de [**desbloqueo**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) , la aplicación realiza el protocolo de enlace necesario, con cualquier mecanismo definido por la MFT. Este paso no está definido por Media Foundation API.
4.  Si el método de [**desbloqueo**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) se realiza correctamente, el MFT se desbloquea.

La aplicación especifica el puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) estableciendo el atributo [MFT \_ FIELDOFUSE \_ Unlock \_ Attribute](mft-fieldofuse-unlock-attribute.md) . Hay varias maneras de establecer este atributo, en función de cómo cree la aplicación el descodificador o la canalización de codificación:



| API                   | Cómo desbloquear el campo de uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lector de origen         | Si su aplicación usa el [lector de origen](source-reader.md) para descodificar un archivo multimedia, establezca el atributo [MFT \_ FIELDOFUSE \_ Unlock \_ ](mft-fieldofuse-unlock-attribute.md) en los parámetros de configuración. Vea [atributos del lector de código fuente](source-reader-attributes.md).                                                                                                                                                                                                                                                                         |
| Escritor de receptor           | Si su aplicación usa el escritor de receptor para codificar un archivo multimedia, establezca el atributo de [ \_ \_ \_ atributo de desbloqueo FIELDOFUSE de MFT](mft-fieldofuse-unlock-attribute.md) en los parámetros de configuración. Vea [atributos del escritor de receptor](sink-writer-attributes.md).                                                                                                                                                                                                                                                                                                    |
| Transcodificación rápida        | Si su aplicación usa la característica de transcodificación rápida para crear una topología de codificación, establezca el [ \_ atributo MFT \_ FIELDOFUSE \_ Unlock](mft-fieldofuse-unlock-attribute.md) al llamar a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Para obtener más información sobre la característica de transcodificación rápida, consulte [Transcode API](transcode-api.md).                                                                                                                                                                      |
| Topología              | Si crea una topología directamente, establezca el atributo de [ \_ \_ desbloqueo \_ FIELDOFUSE de MFT](mft-fieldofuse-unlock-attribute.md) como un atributo en la topología. Consulte [atributos](topology-attributes.md)de la topología.                                                                                                                                                                                                                                                                                                                                                  |
| Objeto de activación de MFT | Si la aplicación enumera directamente los descodificadores o codificadores que va a utilizar, establezca el [ \_ atributo MFT FIELDOFUSE \_ Unlock \_](mft-fieldofuse-unlock-attribute.md) en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . <br/> Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear el MFT. El objeto de activación llama a [**IMFFieldOfUseMFTUnlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) cuando crea la MFT.<br/> |



 

En el diagrama siguiente se muestra la relación entre los objetos de activación de MFT y la interfaz [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .

![diagrama que muestra una aplicación, un objeto de activación y una MFT con flechas a un objeto fou que tiene una flecha de vuelta a MFT](images/mft-fou02.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




