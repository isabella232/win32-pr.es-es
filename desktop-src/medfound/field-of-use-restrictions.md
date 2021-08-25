---
description: Restricciones de campo de uso
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Restricciones de campo de uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccfb5b7c0923bdea117371a3b6af2669bf903fb3af996f754be43d5665c1ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942684"
---
# <a name="field-of-use-restrictions"></a>Restricciones de campo de uso

> [!Note]  
> Este tema se aplica a Windows 7 o posterior.

 

Una *restricción de campo de uso* es una disposición que limita cómo se puede usar una licencia para una tecnología determinada.

Media Foundation proporciona un mecanismo para aplicar restricciones de campo de uso en las transformaciones de Media Foundation (MTA), especialmente los códecs. Este mecanismo requiere que MFT bloquee su propio uso por parte de las aplicaciones hasta que la aplicación haya realizado un protocolo de enlace con MFT. Media Foundation no define el protocolo de enlace; normalmente, implicaría algún tipo de intercambio criptográfico.

### <a name="registration-and-enumeration"></a>Registro y enumeración

Si un MFT tiene restricciones de campo de uso, establezca la marca **\_ \_ \_ FIELDOFUSE de MFT ENUM FLAG** al registrar el MFT. Esta marca se aplica a las siguientes API de registro de MFT:

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

De forma predeterminada, las MTA registradas con esta marca se excluyen de los resultados de enumeración. Para enumerar las MFT con restricciones de campo de uso, llame a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) y especifique la marca **\_ MFT ENUM \_ FLAG \_ FIELDOFUSE** en el *parámetro Flags.* En el siguiente diagrama se muestra este proceso.

![diagrama que muestra mft y una aplicación que envía datos al registro](images/mft-fou01.gif)

La [**función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) siempre excluye cualquier MFTT que tenga restricciones de campo de uso.

### <a name="unlocking-the-mft"></a>Desbloqueo de MFT

Para usar un MFT con restricciones de campo de uso, realice los pasos siguientes:

1.  La aplicación implementa la interfaz [**IMFFieldOfUseMFTUnlock.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)
2.  El [**método IMFFieldOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) toma un puntero a la **interfaz IUnknown** de MFT.
3.  En el [**método Unlock,**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) la aplicación realiza el protocolo de enlace necesario, mediante cualquier mecanismo definido por MFT. Este paso no está definido por Media Foundation API.
4.  Si el [**método Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) se realiza correctamente, MFT se desbloquea a sí mismo.

La aplicación especifica el puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) estableciendo el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ Attribute.](mft-fieldofuse-unlock-attribute.md) Hay varias maneras diferentes de establecer este atributo, en función de cómo la aplicación cree el descodificador o la canalización de codificación:



| API                   | Cómo desbloquear el campo de uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lector de origen         | Si la aplicación usa el Lector de [origen](source-reader.md) para descodificar un archivo multimedia, establezca el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md) en los parámetros de configuración. Vea [Atributos del lector de origen.](source-reader-attributes.md)                                                                                                                                                                                                                                                                         |
| Escritor de receptores           | Si la aplicación usa el escritor de receptores para codificar un archivo multimedia, establezca el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md) en los parámetros de configuración. Vea Sink Writer Attributes (Atributos [del escritor de receptores).](sink-writer-attributes.md)                                                                                                                                                                                                                                                                                                    |
| Transcodificación rápida        | Si la aplicación usa la característica Transcodificación rápida para crear una topología de codificación, establezca el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ al](mft-fieldofuse-unlock-attribute.md) llamar a [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Para obtener más información sobre la característica De transcodificación rápida, consulte [Transcode API](transcode-api.md).                                                                                                                                                                      |
| Topología              | Si crea una topología directamente, establezca el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ ](mft-fieldofuse-unlock-attribute.md) como un atributo en la topología. Vea Topology Attributes ( Atributos [de topología).](topology-attributes.md)                                                                                                                                                                                                                                                                                                                                                  |
| Objeto de activación de MFT | Si la aplicación enumera directamente los descodificadores o codificadores que va a usar, establezca el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md) en los punteros [**DE TIPO IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) <br/> Establezca el atributo antes de llamar [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear el MFT. El objeto de activación llama [**a IMFFieldOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) cuando crea el MFT.<br/> |



 

En el diagrama siguiente se muestra la relación entre los objetos de activación de MFT y la [**interfaz IMFFieldOfUseMFTUnlock.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)

![diagrama que muestra una aplicación, un objeto de activación y mft con flechas a un objeto fou, que tiene una flecha hacia atrás a mft](images/mft-fou02.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




