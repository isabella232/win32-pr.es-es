---
title: Requisitos del sensor para la biometría segura
description: Requisitos del sensor para la biometría segura
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685744"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="82cb4-103">Requisitos del sensor para la biometría segura</span><span class="sxs-lookup"><span data-stu-id="82cb4-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="82cb4-104">Microsoft aprovecha Módulo de plataforma segura (TPM) 2,0 para asegurarse de que, en el hardware adecuado, el software (hasta el malware en el nivel de kernel inclusive) no pueda producir una autenticación biométrica válida si no se proporcionó la biométrica del usuario en el momento de la autenticación.</span><span class="sxs-lookup"><span data-stu-id="82cb4-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="82cb4-105">Para ello, usamos las autorizaciones basadas en sesión TPM 2,0 y el sensor que realiza la extracción de características y la búsqueda de coincidencias en un entorno de ejecución de confianza.</span><span class="sxs-lookup"><span data-stu-id="82cb4-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="82cb4-106">La primera vez que el Plataforma de biometría de Windows ve un sensor seguro (como se muestra en la funcionalidad del sensor seguro), aprovisiona un secreto que se comparte entre el sensor biométrico seguro y el TPM.</span><span class="sxs-lookup"><span data-stu-id="82cb4-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="82cb4-107">Ese secreto nunca se expone de nuevo en el sistema operativo y es único para cada sensor.</span><span class="sxs-lookup"><span data-stu-id="82cb4-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="82cb4-108">Para realizar una autenticación, el Plataforma de biometría de Windows abre una sesión con el TPM y obtiene un nonce.</span><span class="sxs-lookup"><span data-stu-id="82cb4-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="82cb4-109">El nonce se pasa al sensor seguro como parte de una operación de coincidencia segura.</span><span class="sxs-lookup"><span data-stu-id="82cb4-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="82cb4-110">El sensor realiza la coincidencia en el entorno de ejecución de confianza y, si es correcto, calcula un HMAC sobre ese nonce y la identidad del usuario que se identificó.</span><span class="sxs-lookup"><span data-stu-id="82cb4-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="82cb4-111">El Plataforma de biometría de Windows puede usar este HMAC para realizar operaciones criptográficas en el TPM para el usuario que se identificó.</span><span class="sxs-lookup"><span data-stu-id="82cb4-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="82cb4-112">El HMAC es de corta duración y expira después de unos segundos.</span><span class="sxs-lookup"><span data-stu-id="82cb4-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="82cb4-113">Con este protocolo, después del aprovisionamiento inicial, no se incluyen datos confidenciales en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="82cb4-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="82cb4-114">El TPM conserva los secretos y el sensor seguro, y lo único que se expone durante la autenticación es el HMAC de corta duración.</span><span class="sxs-lookup"><span data-stu-id="82cb4-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="82cb4-115">Funcionalidad del sensor seguro</span><span class="sxs-lookup"><span data-stu-id="82cb4-115">Secure sensor capability</span></span>

<span data-ttu-id="82cb4-116">El \_ sensor debe informar de la funcionalidad del sensor seguro de la capacidad de WINBIO \_ si es \_ compatible con los nuevos métodos de adaptador de motor de la versión v 4,0 de la interfaz del adaptador de motor.</span><span class="sxs-lookup"><span data-stu-id="82cb4-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="82cb4-117">Para notificar que un sensor es un sensor seguro, debe cumplir los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="82cb4-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="82cb4-118">El motor de coincidencia del sensor debe estar aislado del sistema operativo normal (por ejemplo, mediante un entorno de ejecución de confianza).</span><span class="sxs-lookup"><span data-stu-id="82cb4-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="82cb4-119">El sensor debe admitir la entrada segura de muestras en el motor de coincidencia aislado; el contenido de los ejemplos nunca debe exponerse al sistema operativo normal.</span><span class="sxs-lookup"><span data-stu-id="82cb4-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="82cb4-120">El motor de coincidencia debe admitir la versión segura de credenciales mediante la implementación de los nuevos métodos V4 descritos a continuación</span><span class="sxs-lookup"><span data-stu-id="82cb4-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="82cb4-121">El sensor debe admitir la detección de ataques de presentación.</span><span class="sxs-lookup"><span data-stu-id="82cb4-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="82cb4-122">El \_ valor del \_ sensor seguro de la capacidad \_ de WINBIO se encuentra en la estructura de [**\_ funcionalidades de WINBIO**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) .</span><span class="sxs-lookup"><span data-stu-id="82cb4-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="82cb4-123">A continuación se muestra un ejemplo de cómo definirlo.</span><span class="sxs-lookup"><span data-stu-id="82cb4-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="82cb4-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="82cb4-124">Error Codes</span></span>


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="82cb4-125">Interfaz del adaptador de motor v 4,0</span><span class="sxs-lookup"><span data-stu-id="82cb4-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="82cb4-126">La versión de la interfaz del adaptador del motor se ha incrementado a 4,0.</span><span class="sxs-lookup"><span data-stu-id="82cb4-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="82cb4-127">Las funciones adicionales de la nueva interfaz permiten al sensor participar en el TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="82cb4-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="82cb4-128">Son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="82cb4-128">They are:</span></span>

-   [<span data-ttu-id="82cb4-129">**EngineAdapterCreateKey**</span><span class="sxs-lookup"><span data-stu-id="82cb4-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="82cb4-130">**EngineAdapterIdentifyFeatureSetSecure**</span><span class="sxs-lookup"><span data-stu-id="82cb4-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a><span data-ttu-id="82cb4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82cb4-131">Requirements</span></span>

<span data-ttu-id="82cb4-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="82cb4-132">Windows 10</span></span>

 

 